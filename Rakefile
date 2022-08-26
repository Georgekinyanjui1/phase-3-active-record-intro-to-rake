namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do 
      puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
  task :hola do
      puts "hola de Rake!"
  end
end

namespace :db do
  task migrate: :environment do
    Student.create_table
  end

  desc "load the environment setup files"
  task :environment do
    require_relative './config/environment'
  end

  task seed: :environment do
    require_relative './db/seeds'
  end
end

desc "drop into the Pry console"
task console: :environment do
  Pry.start
end

desc "load the environment setup files"
task :environment do
  require_relative './config/environment'
end