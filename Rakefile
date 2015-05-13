# Add your own tasks in files placed in lib/tasks ending in .rake,
# for example lib/tasks/capistrano.rake, and they will automatically be available to Rake.

require File.expand_path('../config/application', __FILE__)

Rails.application.load_tasks

require 'dredd/rack'

Dredd::Rack.app = Rails.application
Dredd::Rack::RakeTask.new # run with `rake dredd`

# Optionally, add :dredd to the default task
task default: :dredd # run with `rake`
