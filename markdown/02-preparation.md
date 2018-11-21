<!-- .slide: data-state="normal" id="preparation-packages" data-timing="0" -->
# Preparation: Packages

1. Add project `devel:languages:ruby:extensions` to your repository list
2. Install the packages: `ruby2.5-rubygem-rails-5.2 git apache2 mysql phpMyAdmin` and their dependencies


<!-- .slide: data-state="normal" id="preparation-setting-up-mysql" data-timing="0" -->
# Preparation: Setting up MySQL

1. Start mysql server:

   `rcmysql start`
2. Open a new mysql shell:

   `mysql -u root`
3. Create a user:

   `create user 'admin'@'localhost' identified by 'admin';`
4. Grant privileges to this user:

   `grant all privileges on *.* to 'admin'@'localhost';`
5. Exit from that shell:

   `quit`


<!-- .slide: data-state="normal" id="preparation-apache" data-timing="0" -->
# Preparation: Apache

1. Start the web server:

   `rcapache2 start`
2. Access phpMyAdmin:

   `http://127.0.0.1/phpMyAdmin`


<!-- .slide: data-state="normal" id="preparation-rails" data-timing="0" -->
# Preparation: Ruby on Rails

1. Create a local git repository or one on GitHub/GitLab
2. Create the Rails application:

   `rails -d mysql forum`
3. Enable the `mini_racer` gem
4. Edit `config/database.yml`
5. Setup database with rake: `rake db:create db:setup`
