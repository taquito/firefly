require 'rubygems'
require 'rake'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gemspec|
    gemspec.name = "firefly"
    gemspec.summary = "FireFly is a simple URL shortner for personal use"
    gemspec.description = "FireFly is a simple URL shortner for personal use. It's powered by Sinatra and can be run with any Rack-capable web server."
    gemspec.email = "ariejan@ariejan.net"
    gemspec.homepage = "http://github.com/ariejan/firefly"
    gemspec.authors = ["Ariejan de Vroom"]
    gemspec.rubyforge_project = 'firefly'
    gemspec.add_dependency('sinatra', '~> 1.0')
    gemspec.add_dependency('dm-core', '~> 1.0.2')
    gemspec.add_dependency('dm-migrations', '~> 1.0.2')
    gemspec.add_dependency('dm-transactions', '~> 1.0.2')
    gemspec.add_dependency('dm-aggregates', '~> 1.0.2')
    gemspec.add_dependency('dm-sqlite-adapter', '~> 1.0.2')
    gemspec.add_dependency('haml', '~> 3.0.18')
    gemspec.add_dependency('barby', '~> 0.4.0')
    gemspec.add_dependency('png', '1.1.0')
    
    gemspec.add_development_dependency('rspec', '~> 1.3.0')
    gemspec.add_development_dependency('rack-test', '~> 0.5.4')
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler not available. Install it with: gem install jeweler"
end

require 'spec/rake/spectask'
Spec::Rake::SpecTask.new(:spec) do |spec|
  spec.libs << 'lib' << 'spec'
  spec.spec_files = FileList['spec/**/*_spec.rb']
end

Spec::Rake::SpecTask.new(:rcov) do |spec|
  spec.libs << 'lib' << 'spec'
  spec.pattern = 'spec/**/*_spec.rb'
  spec.rcov = true
end

task :spec => :check_dependencies

task :default => :spec
