# encoding: utf-8

require 'rubygems'
require 'bundler'
begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end
require 'rake'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  # gem is a Gem::Specification... see http://docs.rubygems.org/read/chapter/20 for more options
  gem.name = "give-live-back-to-object"
  gem.homepage = "http://github.com/mixan946/give-live-back-to-object"
  gem.license = "MIT"
  gem.summary = %Q{This gem is provided for easy to use faye in Ruby!}
  gem.description = %Q{
    This Gem is build on top of faye. 
    It has some easy to use helpers like faye_render, faye_subscribe, faye_publish.
  }
  gem.email = "mixan946@yandex.ru"
  gem.authors = ["Mikhail Pospelov"]
  gem.files = Dir.glob('lib/*.rb')

  # dependencies defined in Gemfile
end
Jeweler::RubygemsDotOrgTasks.new

require 'rake/testtask'
Rake::TestTask.new(:test) do |test|
  test.libs << 'lib' << 'test'
  test.pattern = 'test/**/test_*.rb'
  test.verbose = true
end

task :default => :test

require 'rdoc/task'
Rake::RDocTask.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "give-live-back-to-object #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
