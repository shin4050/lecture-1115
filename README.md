# テクノロジー（藤原）11/15授業

## Rails: 実行ログ

```
shin4050:~/workspace/lecture-1115 (master) $ echo -e "install: --no-document\nupdate: --no-document" > ~/.gemrc
shin4050:~/workspace/lecture-1115 (master) $ sudo gem install rails --version "4.2.10"
Fetching: concurrent-ruby-1.0.5.gem (100%)
Successfully installed concurrent-ruby-1.0.5
Fetching: i18n-0.9.1.gem (100%)
Successfully installed i18n-0.9.1
Fetching: thread_safe-0.3.6.gem (100%)
Successfully installed thread_safe-0.3.6
Fetching: tzinfo-1.2.4.gem (100%)
Successfully installed tzinfo-1.2.4
Fetching: activesupport-4.2.10.gem (100%)
Successfully installed activesupport-4.2.10
Fetching: rack-1.6.8.gem (100%)
Successfully installed rack-1.6.8
Fetching: rack-test-0.6.3.gem (100%)
Successfully installed rack-test-0.6.3
Fetching: mini_portile2-2.3.0.gem (100%)
Successfully installed mini_portile2-2.3.0
Fetching: nokogiri-1.8.1.gem (100%)
Building native extensions.  This could take a while...
Successfully installed nokogiri-1.8.1
Fetching: crass-1.0.3.gem (100%)
Successfully installed crass-1.0.3
Fetching: loofah-2.1.1.gem (100%)
Successfully installed loofah-2.1.1
Fetching: rails-html-sanitizer-1.0.3.gem (100%)
Successfully installed rails-html-sanitizer-1.0.3
Fetching: rails-deprecated_sanitizer-1.0.3.gem (100%)
Successfully installed rails-deprecated_sanitizer-1.0.3
Fetching: rails-dom-testing-1.0.8.gem (100%)
Successfully installed rails-dom-testing-1.0.8
Fetching: builder-3.2.3.gem (100%)
Successfully installed builder-3.2.3
Fetching: erubis-2.7.0.gem (100%)
Successfully installed erubis-2.7.0
Fetching: actionview-4.2.10.gem (100%)
Successfully installed actionview-4.2.10
Fetching: actionpack-4.2.10.gem (100%)
Successfully installed actionpack-4.2.10
Fetching: activemodel-4.2.10.gem (100%)
Successfully installed activemodel-4.2.10
Fetching: arel-6.0.4.gem (100%)
Successfully installed arel-6.0.4
Fetching: activerecord-4.2.10.gem (100%)
Successfully installed activerecord-4.2.10
Fetching: globalid-0.4.1.gem (100%)
Successfully installed globalid-0.4.1
Fetching: activejob-4.2.10.gem (100%)
Successfully installed activejob-4.2.10
Fetching: mini_mime-1.0.0.gem (100%)
Successfully installed mini_mime-1.0.0
Fetching: mail-2.7.0.gem (100%)
Successfully installed mail-2.7.0
Fetching: actionmailer-4.2.10.gem (100%)
Successfully installed actionmailer-4.2.10
Fetching: thor-0.20.0.gem (100%)
Successfully installed thor-0.20.0
Fetching: railties-4.2.10.gem (100%)
Successfully installed railties-4.2.10
Fetching: sprockets-3.7.1.gem (100%)
Successfully installed sprockets-3.7.1
Fetching: sprockets-rails-3.2.1.gem (100%)
Successfully installed sprockets-rails-3.2.1
Fetching: rails-4.2.10.gem (100%)
Successfully installed rails-4.2.10
31 gems installed
shin4050:~/workspace/lecture-1115 (master) $ rails new asagao --skip-bundle
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
shin4050:~/workspace/lecture-1115 (master) $ cd asagao/
shin4050:~/workspace/lecture-1115/asagao (master) $ ls
Gemfile  README.rdoc  Rakefile  app/  bin/  config/  config.ru  db/  lib/  log/  public/  test/  tmp/  vendor/
shin4050:~/workspace/lecture-1115/asagao (master) $ bundle install
Fetching gem metadata from https://rubygems.org/..........
Fetching version metadata from https://rubygems.org/..
Fetching dependency metadata from https://rubygems.org/.
Resolving dependencies...
Fetching rake 12.2.1
Installing rake 12.2.1
Using concurrent-ruby 1.0.5
Fetching minitest 5.10.3
Installing minitest 5.10.3
Using thread_safe 0.3.6
Using builder 3.2.3
Using erubis 2.7.0
Using mini_portile2 2.3.0
Using crass 1.0.3
Using rack 1.6.8
Using mini_mime 1.0.0
Using arel 6.0.4
Fetching debug_inspector 0.0.3
Installing debug_inspector 0.0.3 with native extensions
Using bundler 1.15.4
Using byebug 9.1.0
Fetching coffee-script-source 1.12.2
Installing coffee-script-source 1.12.2
Fetching execjs 2.7.0
Installing execjs 2.7.0
Using thor 0.20.0
Fetching ffi 1.9.18
Installing ffi 1.9.18 with native extensions
Fetching multi_json 1.12.2
Installing multi_json 1.12.2
Fetching json 1.8.6
Installing json 1.8.6 with native extensions
Fetching rb-fsevent 0.10.2
Installing rb-fsevent 0.10.2
Fetching rdoc 4.3.0
Installing rdoc 4.3.0
Fetching tilt 2.0.8
Installing tilt 2.0.8
Fetching sqlite3 1.3.13
Installing sqlite3 1.3.13 with native extensions
Fetching turbolinks-source 5.0.3
Installing turbolinks-source 5.0.3
Using i18n 0.9.1
Using tzinfo 1.2.4
Using nokogiri 1.8.1
Using rack-test 0.6.3
Using sprockets 3.7.1
Using mail 2.7.0
Fetching binding_of_caller 0.7.3
Installing binding_of_caller 0.7.3 with native extensions
Fetching coffee-script 2.4.1
Installing coffee-script 2.4.1
Fetching uglifier 3.2.0
Installing uglifier 3.2.0
Fetching rb-inotify 0.9.10
Installing rb-inotify 0.9.10
Fetching sdoc 0.4.2
Installing sdoc 0.4.2
Fetching turbolinks 5.0.1
Installing turbolinks 5.0.1
Using activesupport 4.2.10
Using loofah 2.1.1
Fetching sass-listen 4.0.0
Installing sass-listen 4.0.0
Using rails-deprecated_sanitizer 1.0.3
Using globalid 0.4.1
Using activemodel 4.2.10
Fetching jbuilder 2.7.0
Installing jbuilder 2.7.0
Fetching spring 2.0.2
Installing spring 2.0.2
Using rails-html-sanitizer 1.0.3
Fetching sass 3.5.3
Installing sass 3.5.3
Using rails-dom-testing 1.0.8
Using activejob 4.2.10
Using activerecord 4.2.10
Using actionview 4.2.10
Using actionpack 4.2.10
Using actionmailer 4.2.10
Using railties 4.2.10
Using sprockets-rails 3.2.1
Fetching coffee-rails 4.1.1
Installing coffee-rails 4.1.1
Fetching jquery-rails 4.3.1
Installing jquery-rails 4.3.1
Using rails 4.2.10
Fetching sass-rails 5.0.7
Installing sass-rails 5.0.7
Fetching web-console 2.3.0
Installing web-console 2.3.0
Bundle complete! 12 Gemfile dependencies, 60 gems now installed.
Use `bundle info [gemname]` to see where a bundled gem is installed.
shin4050:~/workspace/lecture-1115/asagao (master) $ rails s -b $IP -p $POST
/usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/server.rb:12:in `parse!': missing argument: -p (OptionParser::MissingArgument)
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/rack-1.6.8/lib/rack/server.rb:316:in `parse_options'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/rack-1.6.8/lib/rack/server.rb:191:in `options'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/server.rb:71:in `set_environment'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/server.rb:55:in `initialize'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:75:in `new'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:75:in `server'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:39:in `run_command!'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands.rb:17:in `<top (required)>'
        from bin/rails:4:in `require'
        from bin/rails:4:in `<main>'
shin4050:~/workspace/lecture-1115/asagao (master) $ bin/rails s -b $IP -p $POST                                                           
/usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/server.rb:12:in `parse!': missing argument: -p (OptionParser::MissingArgument)
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/rack-1.6.8/lib/rack/server.rb:316:in `parse_options'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/rack-1.6.8/lib/rack/server.rb:191:in `options'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/server.rb:71:in `set_environment'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/server.rb:55:in `initialize'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:75:in `new'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:75:in `server'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:39:in `run_command!'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands.rb:17:in `<top (required)>'
        from bin/rails:4:in `require'
        from bin/rails:4:in `<main>'
shin4050:~/workspace/lecture-1115/asagao (master) $ bin/rails s -b $IP
=> Booting WEBrick
=> Rails 4.2.10 application starting in development on http://0.0.0.0:3000
=> Run `rails server -h` for more startup options
=> Ctrl-C to shutdown server
[2017-11-15 01:05:11] INFO  WEBrick 1.3.1
[2017-11-15 01:05:11] INFO  ruby 2.4.0 (2016-12-24) [x86_64-linux]
[2017-11-15 01:05:11] INFO  WEBrick::HTTPServer#start: pid=12871 port=3000
^C[2017-11-15 01:05:14] INFO  going to shutdown ...
[2017-11-15 01:05:14] INFO  WEBrick::HTTPServer#start done.
Exiting
shin4050:~/workspace/lecture-1115/asagao (master) $ bin/rails s -b $IP -p $PORT
=> Booting WEBrick
=> Rails 4.2.10 application starting in development on http://0.0.0.0:8080
=> Run `rails server -h` for more startup options
=> Ctrl-C to shutdown server
[2017-11-15 01:05:22] INFO  WEBrick 1.3.1
[2017-11-15 01:05:22] INFO  ruby 2.4.0 (2016-12-24) [x86_64-linux]
[2017-11-15 01:05:22] INFO  WEBrick::HTTPServer#start: pid=12877 port=8080


Started GET "/" for 125.204.151.95 at 2017-11-15 01:05:44 +0000
Cannot render console from 125.204.151.95! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255
Processing by Rails::WelcomeController#index as HTML
  Rendered /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/templates/rails/welcome/index.html.erb (1.6ms)
Completed 200 OK in 20ms (Views: 11.3ms | ActiveRecord: 0.0ms)
^C[2017-11-15 01:35:33] INFO  going to shutdown ...
[2017-11-15 01:35:33] INFO  WEBrick::HTTPServer#start done.
Exiting
shin4050:~/workspace/lecture-1115/asagao (master) $ touch config/initializers/generators.rb
shin4050:~/workspace/lecture-1115/asagao (master) $ bin/rails g controller top index
      create  app/controllers/top_controller.rb
      invoke  erb
      create    app/views/top
      create    app/views/top/index.html.erb
shin4050:~/workspace/lecture-1115/asagao (master) $ bin/rails s -b $IP -p $PORT
=> Booting WEBrick
=> Rails 4.2.10 application starting in development on http://0.0.0.0:8080
=> Run `rails server -h` for more startup options
=> Ctrl-C to shutdown server
[2017-11-15 02:16:30] INFO  WEBrick 1.3.1
[2017-11-15 02:16:30] INFO  ruby 2.4.0 (2016-12-24) [x86_64-linux]
[2017-11-15 02:16:30] INFO  WEBrick::HTTPServer#start: pid=12960 port=8080


Started GET "/" for 125.204.151.95 at 2017-11-15 02:16:33 +0000
Cannot render console from 125.204.151.95! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255
Processing by TopController#index as HTML
  Rendered top/index.html.erb within layouts/application (4.1ms)
Completed 200 OK in 344ms (Views: 334.6ms | ActiveRecord: 0.0ms)


Started GET "/assets/turbolinks.self-1d1fddf91adc38ac2045c51f0a3e05ca97d07d24d15a4dcbf705009106489e69.js?body=1" for 125.204.151.95 at 2017-11-15 02:16:34 +0000
Cannot render console from 125.204.151.95! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255


Started GET "/assets/application.self-3b8dabdc891efe46b9a144b400ad69e37d7e5876bdc39dee783419a69d7ca819.js?body=1" for 125.204.151.95 at 2017-11-15 02:16:35 +0000
Cannot render console from 125.204.151.95! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255


Started GET "/assets/jquery_ujs.self-784a997f6726036b1993eb2217c9cb558e1cbb801c6da88105588c56f13b466a.js?body=1" for 125.204.151.95 at 2017-11-15 02:16:35 +0000
Cannot render console from 125.204.151.95! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255


Started GET "/assets/jquery.self-bd7ddd393353a8d2480a622e80342adf488fb6006d667e8b42e4c0073393abee.js?body=1" for 125.204.151.95 at 2017-11-15 02:16:35 +0000
Cannot render console from 125.204.151.95! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255


Started GET "/assets/application.self-e80e8f2318043e8af94dddc2adad5a4f09739a8ebb323b3ab31cd71d45fd9113.css?body=1" for 125.204.151.95 at 2017-11-15 02:16:35 +0000
Cannot render console from 125.204.151.95! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255
^C[2017-11-15 02:42:35] INFO  going to shutdown ...
[2017-11-15 02:42:35] INFO  WEBrick::HTTPServer#start done.
Exiting
shin4050:~/workspace/lecture-1115/asagao (master) $ bin/rails s -b $IP -p $PORT
=> Booting WEBrick
=> Rails 4.2.10 application starting in development on http://0.0.0.0:8080
=> Run `rails server -h` for more startup options
=> Ctrl-C to shutdown server
[2017-11-15 02:44:04] INFO  WEBrick 1.3.1
[2017-11-15 02:44:04] INFO  ruby 2.4.0 (2016-12-24) [x86_64-linux]
[2017-11-15 02:44:04] INFO  WEBrick::HTTPServer#start: pid=12995 port=8080


Started GET "/" for 125.204.151.95 at 2017-11-15 02:44:09 +0000
Cannot render console from 125.204.151.95! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255
Processing by TopController#index as HTML
  Rendered top/index.html.erb within layouts/application (1.4ms)
Completed 200 OK in 173ms (Views: 164.1ms | ActiveRecord: 0.0ms)


Started GET "/" for 125.204.151.95 at 2017-11-15 02:46:13 +0000
Cannot render console from 125.204.151.95! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255
Processing by TopController#index as HTML
  Rendered top/index.html.erb within layouts/application (0.4ms)
Completed 200 OK in 38ms (Views: 37.0ms | ActiveRecord: 0.0ms)
^C[2017-11-15 02:50:14] INFO  going to shutdown ...
[2017-11-15 02:50:14] INFO  WEBrick::HTTPServer#start done.
Exiting
shin4050:~/workspace/lecture-1115/asagao (master) $ git config --global user.name "shin4050"
shin4050:~/workspace/lecture-1115/asagao (master) $ git config --global user.email "kd1261465@st.kobedenshi.ac.jp"
```
