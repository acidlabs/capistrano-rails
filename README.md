# Capistrano Rails

Capistrano ready-to-roll recipe examples for Rails with multistage support.

## How to use

```bash
cd /path/to/your/project
git clone git@github.com:acidlabs/capistrano-rails.git cap
cd cap
```

Checkout the examples provided and modify them as they fit.

```bash
cap [environment] deploy:setup
cap [environment] deploy:cold
cap [environment] deploy
```

where *environment* is the environment to which you're going to deploy to.

## Requirements

Depending on the stack you're going to use, you've to add some gems to your project's Gemfile.

```ruby
## Gemfile

# This one is mandatory.
gem 'capistrano'

# If you're using Thin, this should be enough.
gem 'thin'

# The same with Unicorn.
gem 'unicorn'

# If you're going to use foreman to export the upstarts, you should declare it.
gem 'foreman'
```

**That's it**.