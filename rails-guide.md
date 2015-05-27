Rails Guide
===========

## Gemfile setup

Remove sqlite3, add it to the group development

#### Add a group production

      group :production do
        gem 'pg'
        gem 'rails_12factor'
      end

#### Add a group testing

      group :test do
        gem 'minitest-reporters'
        gem 'mini_backtrace'
        gem 'guard'
        gem 'guard-minitest'
      end

Run `bundle install --without production`

## First deployment

1. Add a git repository with `git init`
2. Deploy to Heroku with heroku create
3. Rename the Heroku repository with `heroku rename <name>`
4. Add a [.travis.yml](https://github.com/FalkoJoseph/sample-app/blob/master/.travis.yml) file
5. Set Heroku to automated deployment

## Setup testing environment

#### Include Minitest

    require 'minitest/reporters'
    Minitest::Reporters.use!

#### Add a backtrace silencer under `/config/initializers/backtrace_silencers`

    Rails.backtrace_cleaner.add_silencer { |line| line =~ /rvm/ }

#### Create a Guardfile with `bundle exec guard init` [see example](https://github.com/FalkoJoseph/sample-app/blob/master/Guardfile).

#### Add Spring to the Gitignore with

    # Ignore Spring files
    /spring/*.pid

Start listening to your Guardfile with `bundle exec guard`

## Migrations

#### Create a new table

    rails generate migration CreateProducts name:string part_number:string

#### Add a column

    rails generate migration AddPartNumberToProducts (username:string)

#### Add a column with an index

    rails generate migration AddPartNumberToProducts part_number:string:index

#### Remove a column from a migration

    rails generate migration RemovePartNumberFromProducts

## Generators

#### Create a controller, model, controller, migration and a test

    rails generate scaffold article title:string body:text

#### Create a controller [name], [action]

Also creates a view, helper, test

    rails generate controller Greetings hello

#### Create a model [name], [action]

Also creates a test and migration

    rails generate model Product name:string description:text

#### Create an integration test

    rails generate integration_test user_flows
