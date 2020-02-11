require "rake/testtask"
require "bundler/gem_tasks"
require 'find'

desc 'Say hello'
task :hello do
  puts "Hello there. this is the 'hello' task."
end

desc 'Run tests'
task :default => :test

Rake::TestTask.new(:test) do |t|
  t.libs << "test"
  t.libs << "lib"
  t.test_files = FileList['test/**/*_test.rb']
end

desc 'Display inventor of all files'
task :display_files do
  Find.find(".") do |name|
    puts name if !name.include?("/.") && File.file?(name)
  end
end