Postgres worflow
----------------

1. Creating the database
========================

$createdb chronific

2. Run the database shell
=========================

$psql -U falkojoseph chronific

3. Migrate the database
========================

bin/rake db:create db:migrate
rake db:migrate
