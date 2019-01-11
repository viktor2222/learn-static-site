# learn-static-site

## learn-static-site-middleman

### Installation

<p>Middleman is distributed using the RubyGems package manager. This means you will need both the Ruby language runtime installed and RubyGems to begin using Middleman.</p>


<p>Once you have Ruby and RubyGems up and running, execute the following from the command line:</p>

    $ sudo gem install middleman
    
    check:  $ middleman version
    
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
