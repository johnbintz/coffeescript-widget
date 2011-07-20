require 'rubygems'
require 'coffee_script/source'
require 'erubis'

desc 'build the widget'
task :build do
  mkdir_p 'CoffeeScript.wdgt'
  Dir['src/**/*'].each do |file|
    cp file, 'CoffeeScript.wdgt'
  end
  cp CoffeeScript::Source.bundled_path, 'CoffeeScript.wdgt'
end

