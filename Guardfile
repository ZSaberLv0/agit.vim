# A sample Guardfile
# More info at https://github.com/guard/guard#readme

# Add files and commands to this file, like the example:
#   watch(%r{file/path}) { `command(s)` }
#
notification :libnotify, transient: true, timeout: 1
guard :shell do
  watch(/^(test|autoload|plugin)\/.*\.vim$/) do |m|
    if system('themis --reporter spec')
      n 'success', 'themis', :success
    else
      n 'test failure', 'themis', :failed
    end
  end
end
