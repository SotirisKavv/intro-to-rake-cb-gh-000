desc 'outputs hello to the terminal'
namespace :greeting do
  task :hello do
    puts "hello from Rake!"
  end

  task :hola do
    puts "hola de Rake!"
  end
end


task :console => :environment do
  Pry.start
end

task :environment do
  require_relative './config/environment.rb'
end

namespace :db do
  task :migrate => :environment do
    Student.create_table
  end

  task :seed do
    require_relative './db/seeds.rb'
  end
end
