# UXHannes workstation

This project uses [soloist](https://github.com/mkocher/soloist) and [librarian-chef](https://github.com/applicationsonline/librarian-chef)
to run a subset of the recipes in sprout's cookbooks.

Based on [sprout-wrap](https://github.com/pivotal-sprout/sprout-wrap/). [Fork this repository](https://github.com/hannesjohansson/uxhannes-workstation/fork) to customize its [attributes](http://docs.chef.io/attributes.html) in [soloistrc](/soloistrc) and the list of recipes you'd like to use for your team. You may also want to add other cookbooks to its [Cheffile](/Cheffile), perhaps one of the many [community cookbooks](https://supermarket.chef.io/cookbooks). By default it configures an OS X Mavericks workstation for Ruby development.

Finally, if you've never used Chef before - we highly recommend you buy &amp; watch [this excellent 17 minute screencast](http://railscasts.com/episodes/339-chef-solo-basics) by Ryan Bates.

## Installation under Mavericks (OS X 10.9)

### 1. Install Command Line Tools

    xcode-select --install

If you receive a message about the update server being unavailable and are on Mavericks, then you already have the command line tools.

### 2. Clone this project

    git clone https://github.com/pivotal-sprout/sprout-wrap.git
    cd sprout-wrap

### 3. Install soloist & and other required gems

If you're running under rvm or rbenv, you shouldn't preface the following commands with `sudo`.

    sudo gem install bundler
    bundle

If you receive errors like this:

    clang: error: unknown argument: '-multiply_definedsuppress'

then try downgrading those errors like this:

    sudo ARCHFLAGS=-Wno-error=unused-command-line-argument-hard-error-in-future bundle

### 4. Run soloist

[The `caffeinate` command will keep your computer awake while installing; depending on your network connection, soloist can take from 10 minutes to 2 hours to complete.]

    caffeinate bundle exec soloist

