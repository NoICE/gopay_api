# encoding: utf-8
require 'bundler/gem_tasks'

require 'rake'
require 'rake/testtask'

Rake::TestTask.new do |t|
  t.pattern = 'test/*_test.rb'
  t.ruby_opts << '-I test'
  t.verbose = true
  t.warning = true
end

desc 'Run tests'
task :default => :test

desc 'Uninstall, build and install again'
task :install_gopay do
  sh "gem uninstall gopay"
  sh "gem build gopay.gemspec"
  sh "gem install gopay"
end
