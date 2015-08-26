# attribute_to_mysql
How does Ruby on Rails map it's scaffolded data types to MySQL?

## And the Answer Is ...
<pre>
cd Work
rails new attribute_to_mysql --database=mysql

Microsoft Windows [Version 6.1.7601]
Copyright (c) 2009 Microsoft Corporation.  All rights reserved.

C:\Users\don\Documents\Work>rails new attribute_to_mysql --database=mysql
      create
      create  README.rdoc
      create  Rakefile
      create  config.ru
      create  .gitignore
      create  Gemfile
      create  app
      create  app/assets/javascripts/application.js
      create  app/assets/stylesheets/application.css
      create  app/controllers/application_controller.rb
      create  app/helpers/application_helper.rb
      create  app/views/layouts/application.html.erb
      create  app/assets/images/.keep
      create  app/mailers/.keep
      create  app/models/.keep
      create  app/controllers/concerns/.keep
      create  app/models/concerns/.keep
      create  bin
      create  bin/bundle
      create  bin/rails
      create  bin/rake
      create  bin/setup
      create  config
      create  config/routes.rb
      create  config/application.rb
      create  config/environment.rb
      create  config/secrets.yml
      create  config/environments
      create  config/environments/development.rb
      create  config/environments/production.rb
      create  config/environments/test.rb
      create  config/initializers
      create  config/initializers/assets.rb
      create  config/initializers/backtrace_silencers.rb
      create  config/initializers/cookies_serializer.rb
      create  config/initializers/filter_parameter_logging.rb
      create  config/initializers/inflections.rb
      create  config/initializers/mime_types.rb
      create  config/initializers/session_store.rb
      create  config/initializers/wrap_parameters.rb
      create  config/locales
      create  config/locales/en.yml
      create  config/boot.rb
      create  config/database.yml
      create  db
      create  db/seeds.rb
      create  lib
      create  lib/tasks
      create  lib/tasks/.keep
      create  lib/assets
      create  lib/assets/.keep
      create  log
      create  log/.keep
      create  public
      create  public/404.html
      create  public/422.html
      create  public/500.html
      create  public/favicon.ico
      create  public/robots.txt
      create  test/fixtures
      create  test/fixtures/.keep
      create  test/controllers
      create  test/controllers/.keep
      create  test/mailers
      create  test/mailers/.keep
      create  test/models
      create  test/models/.keep
      create  test/helpers
      create  test/helpers/.keep
      create  test/integration
      create  test/integration/.keep
      create  test/test_helper.rb
      create  tmp/cache
      create  tmp/cache/assets
      create  vendor/assets/javascripts
      create  vendor/assets/javascripts/.keep
      create  vendor/assets/stylesheets
      create  vendor/assets/stylesheets/.keep
         run  bundle install
Fetching gem metadata from https://rubygems.org/............
Fetching version metadata from https://rubygems.org/...
Fetching dependency metadata from https://rubygems.org/..
Resolving dependencies..........
Using rake 10.4.2
Using i18n 0.7.0
Using json 1.8.3
Using minitest 5.8.0
Using thread_safe 0.3.5
Using tzinfo 1.2.2
Using activesupport 4.2.3
Using builder 3.2.2
Using erubis 2.7.0
Using mini_portile 0.6.2
Using nokogiri 1.6.6.2
Using rails-deprecated_sanitizer 1.0.3
Using rails-dom-testing 1.0.7
Using loofah 2.0.3
Using rails-html-sanitizer 1.0.2
Using actionview 4.2.3
Using rack 1.6.4
Using rack-test 0.6.3
Using actionpack 4.2.3
Using globalid 0.3.6
Using activejob 4.2.3
Using mime-types 2.6.1
Using mail 2.6.3
Using actionmailer 4.2.3
Using activemodel 4.2.3
Using arel 6.0.3
Using activerecord 4.2.3
Using debug_inspector 0.0.2
Using binding_of_caller 0.7.2
Using bundler 1.10.5
Using byebug 6.0.2
Using coffee-script-source 1.9.1.1
Using execjs 2.6.0
Using coffee-script 2.4.1
Using thor 0.19.1
Using railties 4.2.3
Using coffee-rails 4.1.0
Using multi_json 1.11.2
Using jbuilder 2.3.1
Using jquery-rails 4.0.4
Installing mysql2 0.3.20
Using sprockets 3.3.3
Using sprockets-rails 2.3.2
Using rails 4.2.3
Using rdoc 4.2.0
Installing sass 3.4.18
Using tilt 1.4.1
Using sass-rails 5.0.3
Using sdoc 0.4.1
Using turbolinks 2.5.3
Using tzinfo-data 1.2015.6
Using uglifier 2.7.1
Using web-console 2.2.1
Bundle complete! 12 Gemfile dependencies, 53 gems now installed.
Use `bundle show [gemname]` to see where a bundled gem is installed.
Post-install message from mysql2:

======================================================================================================

  You've installed the binary version of mysql2.
  It was built using MySQL Connector/C version 6.1.6.
  It's recommended to use the exact same version to avoid potential issues.

  At the time of building this gem, the necessary DLL files were retrieved from:
  http://cdn.mysql.com/Downloads/Connector-C/mysql-connector-c-6.1.6-win32.zip

  This gem *includes* vendor/libmysql.dll with redistribution notice in vendor/README.

======================================================================================================



rem cd attribute_to_mysql
rem Start Up mysql...
rem log in as don using MySQL Workbench, then "create database attribute_to_mysql_development character set='UTF8'"
rem Modify database.yml setting the database username and password to don



rem rails generate scaffold attribute_reference --force

C:\Users\don\Documents\Work\attribute_to_mysql>rails generate scaffold attribute_reference --force
DL is deprecated, please use Fiddle
      invoke  active_record
      create    db/migrate/20150826153206_create_attribute_references.rb
      create    app/models/attribute_reference.rb
      invoke    test_unit
      create      test/models/attribute_reference_test.rb
      create      test/fixtures/attribute_references.yml
      invoke  resource_route
       route    resources :attribute_references
      invoke  scaffold_controller
      create    app/controllers/attribute_references_controller.rb
      invoke    erb
      create      app/views/attribute_references
      create      app/views/attribute_references/index.html.erb
      create      app/views/attribute_references/edit.html.erb
      create      app/views/attribute_references/show.html.erb
      create      app/views/attribute_references/new.html.erb
      create      app/views/attribute_references/_form.html.erb
      invoke    test_unit
      create      test/controllers/attribute_references_controller_test.rb
      invoke    helper
      create      app/helpers/attribute_references_helper.rb
      invoke      test_unit
      invoke    jbuilder
      create      app/views/attribute_references/index.json.jbuilder
      create      app/views/attribute_references/show.json.jbuilder
      invoke  assets
      invoke    coffee
      create      app/assets/javascripts/attribute_references.coffee
      invoke    scss
      create      app/assets/stylesheets/attribute_references.scss
      invoke  scss
      create    app/assets/stylesheets/scaffolds.scss

C:\Users\don\Documents\Work\attribute_to_mysql>rake db:migrate
DL is deprecated, please use Fiddle
== 20150826153206 CreateAttributeReferences: migrating ========================
-- create_table(:attribute_references)
   -> 0.3980s
== 20150826153206 CreateAttributeReferences: migrated (0.4000s) ===============


rails generate scaffold test1 attribute_binary:binary attribute_boolean:boolean attribute_date:date attribute_datetime:datetime attribute_decimal:decimal attribute_float:float attribute_integer:integer attribute_reference:references attribute_string:string attribute_text:text attribute_time:time --force

C:\Users\don\Documents\Work\attribute_to_mysql>rails generate scaffold test1 attribute_binary:binary attribute_boolean:boolean attri
bute_date:date attribute_datetime:datetime attribute_decimal:decimal attribute_float:float attribute_integer:integer attribute_refer
ence:references attribute_string:string attribute_text:text attribute_time:time --force
DL is deprecated, please use Fiddle
      invoke  active_record
      remove    db/migrate/20150826153301_create_test1s.rb
      create    db/migrate/20150826153659_create_test1s.rb
       force    app/models/test1.rb
      invoke    test_unit
   identical      test/models/test1_test.rb
       force      test/fixtures/test1s.yml
      invoke  resource_route
       route    resources :test1s
      invoke  scaffold_controller
       force    app/controllers/test1s_controller.rb
      invoke    erb
       exist      app/views/test1s
       force      app/views/test1s/index.html.erb
   identical      app/views/test1s/edit.html.erb
       force      app/views/test1s/show.html.erb
   identical      app/views/test1s/new.html.erb
       force      app/views/test1s/_form.html.erb
      invoke    test_unit
       force      test/controllers/test1s_controller_test.rb
      invoke    helper
   identical      app/helpers/test1s_helper.rb
      invoke      test_unit
      invoke    jbuilder
       force      app/views/test1s/index.json.jbuilder
       force      app/views/test1s/show.json.jbuilder
      invoke  assets
      invoke    coffee
   identical      app/assets/javascripts/test1s.coffee
      invoke    scss
   identical      app/assets/stylesheets/test1s.scss
      invoke  scss
   identical    app/assets/stylesheets/scaffolds.scss

C:\Users\don\Documents\Work\attribute_to_mysql>rake db:migrate
DL is deprecated, please use Fiddle
== 20150826153659 CreateTest1s: migrating =====================================
-- create_table(:test1s)
   -> 0.2610s
== 20150826153659 CreateTest1s: migrated (0.2630s) ============================



mysql --user=don --password=don attribute_to_mysql_development

mysql> desc test1s;

+------------------------+---------------+------+-----+---------+----------------+
| Field                  | Type          | Null | Key | Default | Extra          |
+------------------------+---------------+------+-----+---------+----------------+
| id                     | int(11)       | NO   | PRI | NULL    | auto_increment |
| attribute_binary       | blob          | YES  |     | NULL    |                |
| attribute_boolean      | tinyint(1)    | YES  |     | NULL    |                |
| attribute_date         | date          | YES  |     | NULL    |                |
| attribute_datetime     | datetime      | YES  |     | NULL    |                |
| attribute_decimal      | decimal(10,0) | YES  |     | NULL    |                |
| attribute_float        | float         | YES  |     | NULL    |                |
| attribute_integer      | int(11)       | YES  |     | NULL    |                |
| attribute_reference_id | int(11)       | YES  | MUL | NULL    |                |
| attribute_string       | varchar(255)  | YES  |     | NULL    |                |
| attribute_text         | text          | YES  |     | NULL    |                |
| attribute_time         | time          | YES  |     | NULL    |                |
| created_at             | datetime      | NO   |     | NULL    |                |
| updated_at             | datetime      | NO   |     | NULL    |                |
+------------------------+---------------+------+-----+---------+----------------+
14 rows in set (0.00 sec)
</pre>