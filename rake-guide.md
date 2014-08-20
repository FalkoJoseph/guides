Rake worflow
------------

1. Get all the routes
=====================

$ rake routes

2. Create a new model
=====================

# Create model
$ bin/rails generate model Post title:string text:text

# Hold a reference of the post
$ bin/rails generate model Comment commenter:string body:text post:references

3. Execute new table
====================

$ bin/rake db:migrate (development)

$ rake db:migrate RAILS_ENV=production (production)
$ rake db:drop:all
$ rake db:create:all
$ rake db:migrate

4. Access the ruby console
==========================

# Start
$ rails c

# Exit
ctrl + d

5. Execute queries in the console
=================================

# Show all entries
$ {tableName}.all

# Create new row
$ {tableName}.create :{row} => 'value'

# Find in row
$ {tableName}.find(id)

6. Create a new controller
==========================

# Create controller
$ bin/rails generate controller Comments

7. Create new migrations
========================

# Create a new migration
$ rails generate migration AddPartNumberToProducts

# Create a new row
$ rails g migration add_username_to_users username:string
