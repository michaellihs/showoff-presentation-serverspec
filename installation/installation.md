!SLIDE title_slide

# Installation & Setup



!SLIDE code_slide

# (1) Familiar with Ruby


    @@@ ruby
    # Within your working directory,
    # create a `Gemfile` with
    source 'http://rubygems.org'

    gem 'serverspec'



    # afterwards, run
    bundle install



!SLIDE code_slide

# (2) Not Familiar with Ruby

    @@@ sh
    gem install serverspec



!SLIDE code_slide

# Initialize Serverspec (SSH)

    @@@ xml
    $ serverspec-init
    Select OS type:

      1) UN*X
      2) Windows

    Select number: 1

    Select a backend type:

      1) SSH
      2) Exec (local)

    Select number: 1

    Vagrant instance y/n: n
    Input target host name: server-name.tld



!SLIDE code_slide

# What you get

    @@@ xml
    .
    ├── Rakefile
    └── spec
        ├── spec_helper.rb
        └── server-name.tld
            └── sample_spec.rb
