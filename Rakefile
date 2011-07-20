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

desc 'build a release widget'
task :release => :build do
  mkdir_p 'pkg'
  system %{tar jcvf pkg/CoffeeScript-#{File.read('VERSION').strip}.tar.bz2 CoffeeScript.wdgt}
  system %{open https://github.com/johnbintz/coffeescript-widget/downloads}
end

