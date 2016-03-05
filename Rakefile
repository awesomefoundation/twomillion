require 'rake'
require 'rake/clean'
require 'rake/task'

output = 'public/_site'
deps = 'node_modules'

CLEAN.include(FileList[output, deps])

desc 'run app'
task :run_app do
  Rake::Task['build:app'].invoke
  Dir.chdir('public') do
    system('jekyll serve -w -H 0.0.0.0 --force_polling')
  end
end

desc 'prepare app for test'
task :test_app do
  Rake::Task['build:app'].invoke
  Dir.chdir('public') do
    system('jekyll serve --detach')
  end
end

namespace :build do
  desc 'run install bower'
  task :npm_install_bower do
    puts 'Installing bower...'
    system('npm install bower')
  end

  desc 'run bower install'
  task :bower_install => :npm_install_bower do
    puts 'Running bower install...'
    system('bower install')
  end

  desc 'run jekyll build'
  task :app => :bower_install do
    Dir.chdir('public') do
      system('jekyll build')
    end
  end
end
