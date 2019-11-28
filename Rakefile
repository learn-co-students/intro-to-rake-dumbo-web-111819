namespace :greeting do 
desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end
 desc 'outputs hola'
  task :hola do 
    puts "hola de Rake!"
  end

end

namespace :db do 


  desc 'create student table in database'
    task :migrate => :environment do 
      Student.create_table
    end

    desc 'calls upon the environment file'
    task :environment do 
      require_relative 'config/environment'
    end

    desc 'seeds database with dummy data from seed file'
    task :seed do 
      require_relative './db/seeds.rb'
    end

end

task :console do 
  Pry.start
end