# learn-static-site

## learn-static-site-middleman

### Installation

<p>Middleman is distributed using the RubyGems package manager. This means you will need both the Ruby language runtime installed and RubyGems to begin using Middleman.</p>
    

<p>Once you have Ruby and RubyGems up and running, execute the following from the command line:</p>

    $ sudo gem install middleman
    
    check:  $ middleman version
    
<p>If you have trouble installing Middleman you need: </p>

    $ sudo apt-get remove ruby
    
<p>After removing ruby. Then reinstall ruby using rbenv and ruby-build according to their docs:</p>
    
    cd $HOME
    sudo apt-get update 
    sudo apt-get install git-core curl zlib1g-dev build-essential libssl-dev libreadline-dev libyaml-dev libsqlite3-dev sqlite3 libxml2-dev libxslt1-dev libcurl4-openssl-dev python-software-properties libffi-dev

    git clone https://github.com/rbenv/rbenv.git ~/.rbenv
    echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc
    echo 'eval "$(rbenv init -)"' >> ~/.bashrc
    exec $SHELL

    git clone https://github.com/rbenv/ruby-build.git ~/.rbenv/plugins/ruby-build
    echo 'export PATH="$HOME/.rbenv/plugins/ruby-build/bin:$PATH"' >> ~/.bashrc
    exec $SHELL

    rbenv install 2.3.1
    rbenv global 2.3.1
    ruby -v
    
    gem install middleman
    
<p>After installing any gems that are binary files, you need to run rbenv rehash</p>

    rbenv rehash
    
After these manipulations, try to install Middleman again</p>
    
<p>This will install Middleman, its dependencies and the command-line tools for using Middleman.</p>

<p>The installation process will add one new command to your environment, with three useful features:</p>

    $ middleman init
    $ middleman server
    $ middleman build
    
### Starting a New Site

<p>To get started we will need to create a project folder for Middleman to work out of. You can do this using an existing folder or have Middleman create one for you using the middleman init command.</p>

    $ middleman init

    $ bundle exec middleman server


<p> First make sure that you have 'middleman-livereload' in your Gemfile. Then simply open your config.rb and add:</p>

    activate :livereload
### Deploying the site

    $ middleman build [--clean]
    $ middleman deploy [--build-before]

### Production Asset Hashing & CDN Configuration

    configure :build do
      activate :minify_css
      activate :minify_javascript

  
      activate :asset_hash

      activate :asset_host, :host => '//YOURDOMAIN.cloudfront.net'
    end
