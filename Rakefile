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

task :console do

end

task :environment do
  require_relative './config/environment'
end

namespace :db do
  desc 'migrate changes to your database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seeds the db with dumy data from a seed file'
  task :seed do
    require_relative './db/seeds.rb'
  end
end

desc 'drop into the Pry console'
task :console => :environment do
  Pry.start
end
