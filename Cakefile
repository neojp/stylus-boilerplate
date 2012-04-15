task 'build', 'Watch source files and build CSS', ->

	# stylus arguments
	options = [
		# add nib support
		'--use', 'nib',

		# watch and compress
		'--compress',
		'--watch'
	]

	# list of files
	files = [
		'site.styl'
	]

	# merge args & files
	args = [].concat options, files

	# spawn the new process
	spawn = require('child_process').spawn
	proc = spawn 'stylus', args # linux/unix version
	proc = spawn 'stylus.cmd', args  if not proc.pid # windows version

	# log output and errors
	logBuffer = (buffer) -> console.log buffer.toString()
	proc.stdout.on 'data', logBuffer
	proc.stderr.on 'data', logBuffer

	# exit process
	proc.on 'exit', (code, signal) ->
		process.exit(1) if code > 0
		console.log 'child process terminated due to receipt of code ' + code