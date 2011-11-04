# Get control of WordPress with version control #

## Overview ##

This presentation will help you get your WordPress sites, plugins, and themes under control with version control. Learn the finer points of tools like Subversion and Git.  And find out how to share your code with the community for collaboration.

Presented at [WordCamp Philly 2011](http://2011.philly.wordcamp.org/)

Put together by [Dave Konopka](http://davekonopka.com). On Twitter: [@davekonopka](http://twitter.com/davekonopka)

### Version Control ###

* Why bother with version control?
* Tools: The options
* WordPress under control
* Workflows
* Q & A

## Version Control ##

### Why Bother? ###

* Work with a net
* Manage streams of work
* Collaborate (even if only with your future self)
* Synchronize between people and environments

### A version control refresher ###

* Respository
* Code lines
* Commits
* Tags
* Branching, merging
* Diffs, patching
* Remotes

## Tools: The options ##

### Subversion ###

* WordPress is heavily invested in SVN
    * WordPress code, plugin directory
* Doesn't mean you need to use SVN
* Centralized
    * Must be connect to repository to work
* Slower
* Painful branching

### Git ###

* Popular
    * 163K Ubuntu package installs as of October 2011
    * Included with OSX dev tools
* Github
    * 1 million+ users
    * Linux, Ruby on Rails, jQuery, etc… hosted
* Distributed
    * Work disconnected
    * Connect when you want
* Faster
* Shape your history
* Easy branching

### Some Git terms ###

* Command line is your friend, learn there if you can then go gui
* Git is a collection of command line tools
* .git folder
* Clone
* Staging area
* Remotes
* Push/pull

## WordPress: Under control ##

### Manage custom plugins, themes ###

* Clone = install
* Push from dev, pull on server

#### Publishing to WordPress plugins directory ####

* Each plugin is an SVN repo
    * Latest trunk or specified tag zipped up every 15 minutes
* git-svn
* Use diff tool to apply changes to SVN checkout
* Publish to Github for additional exposure

### Manage an entire WordPress site ###

* Site is a repo
    * Master = WordPress code
    * MySite branch = customizations
* SVN externals
* Git submodules
* Ignore dynamic pieces
    * wp-content/uploads
    * wp-config.php
    * etc…
* Workflow of applying WordPress updates
    * Checkout master, delete all files, post code
    * Commit
    * Checkout working branch, merge in master

### Contributing to projects ###

* Patches
    * SVN patches
    * Git patches
* Github
    * Fork a repo
    * Go wild in your fork
    * Submit pull requests

### Deploy ###

* Manual pull on server
* Remote git repo, push updates code
* Capistrano (Ruby gem)
* Post commit hooks

### Databases ###

* Version control does not serve databases well
* Mysqldump, track script
* Plugins for managing data migration

## Workflows: Pleasure principal ##

* Keep public branches clean, be thoughtful with commits
* Branch all the time
* Feature branch
    * Create a branch
    * Commit as often as you want
    * Once ready to ship, clean up the branch history
    * Merge in a single, or a few, clean atomic commits

## Resources ##

### Hosted services ###

* [Github](https://github.com/) 
    * Hosted Git repos, free public repos
    * Collaboration & projest management tools
* [Beanstalk](http://beanstalkapp.com/)
    * Hosted Subversion, Git repos
    * Collaboration & project management tools
    * Philly based company
* [Unfuddle](http://unfuddle.com/)
    * Hosted Subversion, Git repos
    * Free _private_ repos
    * Collaboration & project management tools

### Guides ###

* [Beanstalk Guides](http://guides.beanstalkapp.com/) "Everything you
  need to get started with Subversion or Git."
* [Github Help](http://help.github.com/)

### Applications ###

#### SVN ####

* [RapidSVN](http://rapidsvn.tigris.org/) Cross platform SVN gui
* [Versions](http://versionsapp.com/) OS X SVN gui
* [TortoiseSVN](http://tortoisesvn.net/) Windows SVN tool

#### Git ####

* [GitX (L)](http://gitx.laullon.com/) OS X Git gui
* [Github for Mac](http://mac.github.com/) OS X Git gui
* [TortoiseGit](http://code.google.com/p/tortoisegit/) Windows Git tool

## Credits ##

### Photographs ###

* [Bear falling](http://missoulaeditor.com/?p=2154)
* [Lasers](http://www.flickr.com/photos/arthur_pewty/1537991764/)
* [Future self](http://www.flickr.com/photos/72213316@N00/6212937263/)
* [Synchronize](http://www.flickr.com/photos/paulpker121/3536517924/)

