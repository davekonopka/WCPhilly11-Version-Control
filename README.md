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
* Commitment: You have to commit to using version control to get
  benefits

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
    * 1 million users on Github
    * 163K Ubuntu package installs according to popcon
    * Included with OSX dev tools
* Github
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
    * [Publish git respository to svn easily](http://stas.nerd.ro/index.php/read/861)
* Use diff tool to apply changes to SVN checkout
    * FileMerge on Mac OS X
    * [DiffMerge](http://en.wikipedia.org/wiki/Apple_Developer_Tools#FileMerge) Win, Mac, Linux
    * [WinMerge](http://winmerge.org/) Windows
* Publish to Github for additional exposure

### Manage an entire WordPress site ###

* Site is a repo
    * Master = WordPress code
    * MySite branch = customizations
* [SVN externals](http://svnbook.red-bean.com/en/1.6/svn.advanced.externals.html)
* [Git submodules](http://book.git-scm.com/5_submodules.html)
* Ignore dynamic pieces
    * wp-content/uploads
    * wp-config.php
    * etc…
* Workflow of applying WordPress updates
    * Checkout master, delete all files, post code
    * Commit
    * Checkout working branch, merge in master
* [WordPress on Github](https://github.com/markjaquith/WordPress)

### Contributing to projects ###

* Patches
    * [SVN patches](http://codex.wordpress.org/Using_Subversion#Saving_patch.2Fdiff_files)
    * [Git patches](http://book.git-scm.com/5_git_and_email.html)
* Github
    * Fork a repo
    * Go wild in your fork
    * Submit pull requests
    * Gists

### Deploy ###

* Manual pull on server
* Remote git repo, push updates code
* Capistrano, Chef
    * [WordPress Capistrano](https://github.com/jestro/wordpress-capistrano)
    * [Deploying WordPress with Capistrano](http://theme.fm/2011/08/tutorial-deploying-wordpress-with-capistrano-2082/)
    * [WordPress Chef Cookbook](http://community.opscode.com/cookbooks/wordpress)
    * [Deploy WordPress to Amazon EC2 Micro Instance with Opscode
      Chef](http://blog.ibd.com/howto/deploy-wordpress-to-amazon-ec2-micro-instance-with-opscode-chef/)
* Post commit hooks
    * [Github Post-Receive Hooks](http://help.github.com/post-receive-hooks/)
    * [Beanstalk Web Hooks](http://support.beanstalkapp.com/customer/portal/articles/68110-trigger-a-url-on-commit-with-web-hooks)

### Databases ###

* Version control does not serve databases well
* Mysqldump, track script
* Plugins for managing data/content migration
    * [DeployMint](http://markmaunder.com/2011/08/19/deploymint-a-staging-and-deployment-system-for-wordpress/)
    * [RAMP](http://crowdfavorite.com/wordpress/ramp/)
    * [BackupBuddy](http://pluginbuddy.com/purchase/backupbuddy/)

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
* [BitBucket](https://bitbucket.org/)
    * _Unlimited_ free private respositories
* [Unfuddle](http://unfuddle.com/)
    * Hosted Subversion, Git repos
    * Free _private_ repos
    * Collaboration & project management tools

### Guides ###

* [Beanstalk Guides](http://guides.beanstalkapp.com/) "Everything you
  need to get started with Subversion or Git."
* [Github Help](http://help.github.com/)
* [Version Control with Subversion](http://svnbook.red-bean.com/) free
  book
* [The Git Community Book](http://book.git-scm.com/)
* [Pro Git](http://progit.org/book/) free book
* [Git Magic](http://www-cs-students.stanford.edu/~blynn/gitmagic/)
* [Think Like (a) Git](http://think-like-a-git.net/)
* [git ready](http://gitready.com/)
* [Git Is Simpler Than You Think](http://nfarina.com/post/9868516270/git-is-simpler)
* [WordPress Codex: Using Subversion](http://codex.wordpress.org/Using_Subversion)

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

