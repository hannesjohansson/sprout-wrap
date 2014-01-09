# UXhannes OSX-sprout (sprout-wrap)

This project is used to setup my OSX development machine. It's a fork of [sprout-wrap](https://github.com/pivotal-sprout/sprout-wrap/fork) complimented with [sprout-homebrew](https://github.com/pivotal-sprout/sprout-homebrew).

[Fork it](https://github.com/hannesjohansson/sprout-wrap/fork) to 
customize its [attributes](http://docs.opscode.com/chef_overview_attributes.html) in [soloistrc](/soloistrc) and the list of recipes 
you'd like to use for your team. You may also want to add other cookbooks to its [Cheffile](/Cheffile), perhaps one 
of the many [community cookbooks](http://community.opscode.com/cookbooks). To add homebrew casks (which also are pre-bundled OSX apps), check out [homebrew-cask](https://github.com/phinze/homebrew-cask/tree/master/Casks). The casks are specified last in the soloistrc file.

## Installation under Mavericks (OS X 10.9)

### 1. Install XCode

[![Xcode - Apple](http://r.mzstatic.com/images/web/linkmaker/badge_macappstore-lrg.gif)](https://itunes.apple.com/us/app/xcode/id497799835?mt=12&uo=4)

Don't forget to start up Xcode once it's installed so that you can agree to the terms&mdash;many commands won't work until the terms have been agreed to.

### 2. Install Command Line Tools
  
    xcode-select --install
  
### 3. Clone this project

    git clone https://github.com/hannesjohansson/sprout-wrap.git
    cd sprout-wrap

### 4. Install soloist & and other required gems

If you're running under rvm or rbenv, you shouldn't preface the following commands with `sudo`.

    sudo gem install bundler
    sudo bundle

### 5. Run soloist

[You may want to modify your Energy Saver preferences (**System Preferences &rarr; Energy Saver &rarr; Computer Sleep &rarr; 3hrs**) because soloist usually takes 2-3 hours to complete.]

    bundle exec soloist

