# テクノロジー（藤原）11/15授業

## Rails: 実行ログ

```
seno2:~/workspace $ cd ~/workspace
seno2:~/workspace $ git clone git@github.com:seno2/lecture-1115.git
Cloning into 'lecture-1115'...
Warning: Permanently added 'github.com,192.30.253.113' (RSA) to the list of known hosts.
remote: Counting objects: 6, done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 6 (delta 0), reused 6 (delta 0), pack-reused 0
Receiving objects: 100% (6/6), done.
seno2:~/workspace $ cd ~/workspace/lecture-1115
seno2:~/workspace/lecture-1115 (master) $  rails new asagao --skip-bundle
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
      create  config/initializers/to_time_preserves_timezone.rb
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
seno2:~/workspace/lecture-1115 (master) $ cd asagao
seno2:~/workspace/lecture-1115/asagao (master) $ ls
Gemfile  README.rdoc  Rakefile  app/  bin/  config/  config.ru  db/  lib/  log/  public/  test/  tmp/  vendor/
seno2:~/workspace/lecture-1115/asagao (master) $ bundle install
The latest bundler is 1.16.0, but you are currently running 1.15.4.
To update, run `gem install bundler`
Fetching gem metadata from https://rubygems.org/..........
Fetching version metadata from https://rubygems.org/..
Fetching dependency metadata from https://rubygems.org/.
Resolving dependencies...
Using rake 12.2.1
Using concurrent-ruby 1.0.5
Using minitest 5.10.3
Using thread_safe 0.3.6
Using builder 3.2.3
Using erubis 2.7.0
Using mini_portile2 2.3.0
Fetching crass 1.0.3
Installing crass 1.0.3
Using rack 1.6.8
Fetching mini_mime 1.0.0
Installing mini_mime 1.0.0
Using arel 6.0.4
Using debug_inspector 0.0.3
Using bundler 1.15.4
Using byebug 9.1.0
Fetching coffee-script-source 1.12.2
Installing coffee-script-source 1.12.2
Using execjs 2.7.0
Using thor 0.20.0
Using ffi 1.9.18
Using multi_json 1.12.2
Fetching json 1.8.6
Installing json 1.8.6 with native extensions
Using rb-fsevent 0.10.2
Using rdoc 4.3.0
Using tilt 2.0.8
Using sqlite3 1.3.13
Using turbolinks-source 5.0.3
Using i18n 0.9.1
Using tzinfo 1.2.4
Using nokogiri 1.8.1
Using rack-test 0.6.3
Using sprockets 3.7.1
Using mail 2.7.0
Using binding_of_caller 0.7.3
Using coffee-script 2.4.1
Using uglifier 3.2.0
Using rb-inotify 0.9.10
Using sdoc 0.4.2
Using turbolinks 5.0.1
Using activesupport 4.2.10
Using loofah 2.1.1
Using sass-listen 4.0.0
Using rails-deprecated_sanitizer 1.0.3
Using globalid 0.4.1
Using activemodel 4.2.10
Using jbuilder 2.7.0
Using spring 2.0.2
Using rails-html-sanitizer 1.0.3
Using sass 3.5.3
Using rails-dom-testing 1.0.8
Using activejob 4.2.10
Using activerecord 4.2.10
Using actionview 4.2.10
Using actionpack 4.2.10
Using actionmailer 4.2.10
Using railties 4.2.10
Using sprockets-rails 3.2.1
Using coffee-rails 4.1.1
Using jquery-rails 4.3.1
Using rails 4.2.10
Fetching sass-rails 5.0.7
Installing sass-rails 5.0.7
Using web-console 2.3.0
Bundle complete! 12 Gemfile dependencies, 60 gems now installed.
Use `bundle info [gemname]` to see where a bundled gem is installed.
seno2:~/workspace/lecture-1115/asagao (master) $ bin/rails s -b $IP -p $PORT
=> Booting WEBrick
=> Rails 4.2.10 application starting in development on http://0.0.0.0:8080
=> Run `rails server -h` for more startup options
=> Ctrl-C to shutdown server
[2017-11-15 00:32:58] INFO  WEBrick 1.3.1
[2017-11-15 00:32:58] INFO  ruby 2.4.0 (2016-12-24) [x86_64-linux]
[2017-11-15 00:32:58] INFO  WEBrick::HTTPServer#start: pid=1906 port=8080


Started GET "/" for 125.204.151.95 at 2017-11-15 00:33:30 +0000
Cannot render console from 125.204.151.95! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255
Processing by Rails::WelcomeController#index as HTML
  Rendered /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/templates/rails/welcome/index.html.erb (2.2ms)
Completed 200 OK in 23ms (Views: 14.3ms | ActiveRecord: 0.0ms)
^C[2017-11-15 00:33:50] INFO  going to shutdown ...
[2017-11-15 00:33:50] INFO  WEBrick::HTTPServer#start done.
Exiting
seno2:~/workspace/lecture-1115/asagao (master) $ which rails
/usr/local/rvm/rubies/ruby-2.4.0/bin/rails
seno2:~/workspace/lecture-1115/asagao (master) $  which bin/rails
bin/rails
seno2:~/workspace/lecture-1115/asagao (master) $ touch config/initializers/generators.rb
seno2:~/workspace/lecture-1115/asagao (master) $ bin/rails g controller top index
      create  app/controllers/top_controller.rb
       route  get 'top/index'
      invoke  erb
      create    app/views/top
      create    app/views/top/index.html.erb
      invoke  test_unit
      create    test/controllers/top_controller_test.rb
      invoke  helper
      create    app/helpers/top_helper.rb
      invoke    test_unit
      invoke  assets
      invoke    coffee
      create      app/assets/javascripts/top.coffee
      invoke    scss
      create      app/assets/stylesheets/top.scss
seno2:~/workspace/lecture-1115/asagao (master) $ bin/rails s -b $IP -p $PORT
=> Booting WEBrick
=> Rails 4.2.10 application starting in development on http://0.0.0.0:8080
=> Run `rails server -h` for more startup options
=> Ctrl-C to shutdown server
[2017-11-15 00:47:40] INFO  WEBrick 1.3.1
[2017-11-15 00:47:40] INFO  ruby 2.4.0 (2016-12-24) [x86_64-linux]
[2017-11-15 00:47:40] INFO  WEBrick::HTTPServer#start: pid=1955 port=8080


Started GET "/" for 125.204.151.95 at 2017-11-15 00:54:01 +0000
Cannot render console from 125.204.151.95! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255
Processing by TopController#index as HTML
  Rendered top/index.html.erb within layouts/application (1.5ms)
Completed 200 OK in 767ms (Views: 758.4ms | ActiveRecord: 0.0ms)


Started GET "/assets/top.self-e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855.css?body=1" for 125.204.151.95 at 2017-11-15 00:54:02 +0000
Cannot render console from 125.204.151.95! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255


Started GET "/assets/turbolinks.self-1d1fddf91adc38ac2045c51f0a3e05ca97d07d24d15a4dcbf705009106489e69.js?body=1" for 125.204.151.95 at 2017-11-15 00:54:02 +0000
Cannot render console from 125.204.151.95! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255


Started GET "/assets/top.self-877aef30ae1b040ab8a3aba4e3e309a11d7f2612f44dde450b5c157aa5f95c05.js?body=1" for 125.204.151.95 at 2017-11-15 00:54:02 +0000
Cannot render console from 125.204.151.95! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255


Started GET "/assets/jquery.self-bd7ddd393353a8d2480a622e80342adf488fb6006d667e8b42e4c0073393abee.js?body=1" for 125.204.151.95 at 2017-11-15 00:54:03 +0000
Cannot render console from 125.204.151.95! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255


Started GET "/assets/application.self-e80e8f2318043e8af94dddc2adad5a4f09739a8ebb323b3ab31cd71d45fd9113.css?body=1" for 125.204.151.95 at 2017-11-15 00:54:03 +0000
Cannot render console from 125.204.151.95! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255


Started GET "/assets/jquery_ujs.self-784a997f6726036b1993eb2217c9cb558e1cbb801c6da88105588c56f13b466a.js?body=1" for 125.204.151.95 at 2017-11-15 00:54:03 +0000
Cannot render console from 125.204.151.95! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255


Started GET "/assets/application.self-3b8dabdc891efe46b9a144b400ad69e37d7e5876bdc39dee783419a69d7ca819.js?body=1" for 125.204.151.95 at 2017-11-15 00:54:03 +0000
Cannot render console from 125.204.151.95! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255


Started GET "/" for 125.204.151.95 at 2017-11-15 00:57:33 +0000
Cannot render console from 125.204.151.95! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255
Processing by TopController#index as HTML
  Rendered top/index.html.erb within layouts/application (0.4ms)
Completed 200 OK in 16ms (Views: 15.4ms | ActiveRecord: 0.0ms)


Started GET "/" for 125.204.151.95 at 2017-11-15 00:58:14 +0000
Cannot render console from 125.204.151.95! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255
Processing by TopController#index as HTML
  Rendered top/index.html.erb within layouts/application (0.1ms)
Completed 200 OK in 16ms (Views: 15.8ms | ActiveRecord: 0.0ms)
^C[2017-11-15 00:58:28] INFO  going to shutdown ...
[2017-11-15 00:58:28] INFO  WEBrick::HTTPServer#start done.
Exiting
```
