# Setup

Clone the demo repository.

`git clone git@github.com:michikono/php-bdd-demo.git`

Install xcode command line utilities if you do not have them already

`xcode-select --install`

### Install Composer

`brew tap josegonzalez/homebrew-php`

`brew install josegonzalez/php/composer`

### install PHP54

`brew tap homebrew/dupes`

`brew tap josegonzalez/homebrew-php`

`brew install php55`

the previous step will tell you HOW to update your CLI path, which is also outlined below!

edit your ~/.bashrc file:
`export PATH="$(brew --prefix josegonzalez/php/php54)/bin:$PATH"`

update your paths
`source ~/.bashrc `

### install rvm and ruby
`curl -sSL https://get.rvm.io | bash`
`rvm install ruby-2.1.0`
`rvm reload`
`bundle install`

### setup auto-test functionality

`gem install watchr`

Event watcher for Linux/BSD:

`gem install rev`

Event watcher for OSX:

`gem install ruby-fsevent`

### Install dependencies PHPUnit and PHPUnit_Selenium:

Navigate into folder where code is pulled

`composer install`

Or if asked to run it:

`composer update`

# Run test framework

In a new tab: run the selenium grid script

`./bin/selenium-hub.sh`

In another tab:

`./bin/selenium-webdriver.sh`

Turn on auto test-running (runs headless behat tests):

`observr ./test.observr.rb`

# Optional steps

Run behat tests

`./bin/behat --verbose --profile headless`

Or for the full browser test

`./bin/behat --verbose`

