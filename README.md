Dredd::Rack Rails Example
=========================

Demonstrate the [Dredd::Rack][dredd-rack] usage in a Rails app.

  [dredd-rack]: https://github.com/gonzalo-bulnes/dredd-rack

Usage
-----

```bash
# run the app
rackup -p 3000
```

### How-to add Dredd::Rack to a Rails application

1. Store the API blueprints in the `doc` directory, with the `.apib` or `.apib.md` extension
1. Install Dredd::Rack (see the [Dredd::Rack documentation][dredd-rack])
1. Add the `dredd` task to your `Rakefile`

Example:

```ruby
# Gemfile

gem 'dredd-rack', '0.4.0'
```

```ruby
# Rakefile

# ...

require 'dredd/rack'

Dredd::Rack.app = Rails.application # put here the name of your app
Dredd::Rack::RakeTask.new # run with `rake dredd`

# Optionally, add :dredd to the default task
task default: :dredd # run with `rake`
```

That's all!

Documentation
-------------

See the [Dredd::Rack Rails Example API blueprint][doc] (`doc/app.apib.md`) for an always up-to-date documentation of this example API. Note how the `.apib.md` extension allows to read the documentation on Github : )

  [doc]: doc/app.apib.md

Development
-----------

```bash
# run the app
rerun 'rackup --port=3000'
```
