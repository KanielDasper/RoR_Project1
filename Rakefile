# Add your own tasks in files placed in lib/tasks ending in .rake,
# for example lib/tasks/capistrano.rake, and they will automatically be available to Rake.

require_relative 'config/application'

Rails.application.load_tasks

# Rakefile
# # Rakefile

# Load the Rails application environment

namespace :db do
  desc 'Check database connection'
  task check_connection: :environment do
    ActiveRecord::Base.connection.active?
    puts 'Connection to the database is active.'
  rescue ActiveRecord::NoDatabaseError
    puts 'Database does not exist.'
  rescue ActiveRecord::StatementInvalid => e
    puts "Error connecting to the database: #{e.message}"
  end
end
