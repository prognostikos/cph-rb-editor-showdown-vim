!SLIDE
# Editor Showdown - Vim! #

![Vim logo](vim-animated.gif)

Copenhagen Ruby Brigade<br/>
10 Jan 2012

Matt Rohrer<br/>
[matt@prognostikos.com](mailto:matt@prognostikos.com)<br/>
[http://prognostikos.com](http://prognostikos.com)

!SLIDE transition=fade

# I started as unix admin years ago, which probably why I ♥ Vim...

!SLIDE incremental transition=fade

# But here are some reasons why YOU should ♥ Vim:

  - ubiquity (platforms & programming languages)
  - "vim is forever" (20 years and counting)
  - [text objects](http://blog.carbonfive.com/2011/10/17/vim-text-objects-the-definitive-guide/) and other movement commands
  - split & vsplit

!SLIDE incremental transition=fade
# Not to rekindle a holy war, but why not the other ancient editor?

  - speed (startup, etc)
  - modal editing (RSI)
  - but really, either is fine

!SLIDE incremental transition=fade
# Quick survey

  - How many people here use vim? 
  - As a programming editor, not a configuration file editor?
  - How many people have only memorized :q?
  - How many people would like to try vim but are scared?

!SLIDE incremental transition=fade
# My development setup 

  - iTerm2
  - rbenv, ruby-build, rbenv-gemset
  - tmux w/tmuxinator

!SLIDE incremental transition=fade
# My development setup, p.2

  - MacVim
  - guard with guard-spork, guard-rspec & guard-cucumber
  - rails c
  - rails db

!SLIDE incremental transition=fade
# My Vim configuration

  - [Hosted on github](https://github.com/prognostikos/mmr_config_files)
  - CREDITS: [@mislav](https://github.com/mislav) [@amix](https://github.com/amix) [@garybernhardt](https://github.com/garybernhardt)
  - plugins as git submodules, managed by pathogen
  - shell script wrapper to start Command-T if no file given

!SLIDE incremental transition=fade
# My Vim configuration, p.2

    @@@ Shell
    #!/bin/sh
    [[ -z $@ ]] && cmd='-c :CommandT'
    exec mvim -v $cmd $@

!SLIDE commandline transition=fade
# My Vim plugins

    $ ls ~/.vim/bundle

    vim-coffee-script vim-colors-solarized vim-command-t 
    vim-commentary vim-endwise vim-fugitive vim-javascript 
    vim-jst vim-markdown vim-pathogen vim-rails vim-ruby 
    vim-ruby-refactoring vim-supertab vim-xmledit

!SLIDE incremental transition=fade
# Rails.vim

  - `gf` (goto file)
  - `:A` (alternate file)
  - `:AV` mapped to `<leader>av` for vsplit
  - `:AS` mapped to `<leader>as` for split

!SLIDE incremental transition=fade
# Rails.vim, p.2

  - `:Rmigration` (opens the latest migration)
  - `:Rmigration <substring>` (finds a migration with substring)

!SLIDE incremental transition=fade
# Rails.vim, p.3

  - `:Rake`
  - runs test on test files
  - runs migrations on migration files

!SLIDE incremental transition=fade
# Rails.vim, p.4

  - `:help rails-refactoring`
  - `:help rails` (in general)

!SLIDE incremental transition=fade
# fugitive.vim (Git)

  - `:Gmove`
  - `:Gstatus` with diff, add, commit, etc

!SLIDE incremental transition=fade
# snipMate

  - `def<Tab>`
  - `collection.sel<Tab>`

!SLIDE incremental transition=fade
# Movement

  - `gg` `gi` (go to top of file, go back to last instert position)
  - `crtl-o` & `ctrl-i` (switch between jumps)
  
!SLIDE incremental transition=fade
# Registers

  - `"a-z` (named)
  - `"0` (last yank)
  - `"1-9` (last delete or change)
  - `"+` (system keyboard contents - doesn't work for me with tmux)

!SLIDE incremental transition=fade
# What I know Vim can do, but I have not yet explored:

  - Ruby Refactoring [1](https://github.com/ecomba/vim-ruby-refactoring) [2](http://justinram.wordpress.com/2010/12/30/vim-ruby-refactoring-series/)
  - Ruby Debugging [1](https://github.com/astashov/vim-ruby-debugger)

!SLIDE
# Resources for beginners

  - [http://openvim.com/](http://openvim.com/)
  - `vimtutor`
  - `:help`
  - [http://mislav.uniqpath.com/2011/12/vim-revisited/](http://mislav.uniqpath.com/2011/12/vim-revisited/)

!SLIDE smbullets
# Additional resources

  - [The Vim learning curve is a myth](http://robots.thoughtbot.com/post/13164810557/the-vim-learning-curve-is-a-myth)
  - [Write Code Faster - Expert Level Vim](http://bostonrb.org/presentations/write-code-faster-expert-level-vim)
  - [Vim Macros and You](http://robots.thoughtbot.com/post/15348543318/vim-macros-and-you)
  - [Github VimL Twitter feed](https://twitter.com/#!/github_viml)
  - [Destroy all Software](http://destroyallsoftware.com) (several screencasts, also great testing/ruby stuff)
  - [Peepcode](http://peepcode.com) (two vim screencasts)

!SLIDE
# Questions?

Matt Rohrer<br/>
[matt@prognostikos.com](mailto:matt@prognostikos.com)<br/>
[http://prognostikos.com](http://prognostikos.com)

!SLIDE
# Thanks!
