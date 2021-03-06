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
  gem.name = "tumblr-oauth"
  gem.homepage = "http://github.com/shir/tumblr-oauth"
  gem.license = "MIT"
  gem.summary = %Q{Tumblr library with OAuth support}
  gem.description = %q{A Ruby wrapper for Tumblr AOuth API}
  gem.email = "shaynurov@gmail.com"
  gem.authors = ["Ildar Shaynurov"]
  # dependencies defined in Gemfile
end
Jeweler::RubygemsDotOrgTasks.new

require 'rspec/core'
require 'rspec/core/rake_task'
RSpec::Core::RakeTask.new(:spec) do |spec|
  spec.pattern = FileList['spec/**/*_spec.rb']
end

RSpec::Core::RakeTask.new(:rcov) do |spec|
  spec.pattern = 'spec/**/*_spec.rb'
  spec.rcov = true
end

task :default => :spec

require 'rdoc/task'
require File.expand_path('../lib/tumblr-oauth/version', __FILE__)

RDoc::Task.new do |rdoc|
  version = TumblrOAuth::VERSION

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "tumblr-oauth #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
