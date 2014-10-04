# Hyde Away

My installation of Jekyll on Windows 8.1 x32

Install Git Bash

Install Ruby

Install Jekyll

## Installation Requirements

<code>
myname@myPC /my/site

$ ruby --version

ruby 2.1.3p242 (2014-09-19 revision 47630) [i386-mingw32]
</code>

<code>
$ bash
bash-3.1$ help

GNU bash, version 3.1.20(4)-release (i686-pc-msys)
</code>

Use Ctrl-D to exit GNU bash

<code>
$ git --version

git version 1.9.4.msysgit.2
</code>

## Installation Process

<code>
$ gem install jekyll

Successfully installed jekyll-2.4.0

Parsing documentation for jekyll-2.4.0

Installing ri documentation for jekyll-2.4.0

Done installing documentation for jekyll after 8 seconds

1 gem installed

$ jekyll new mysite

New jekyll site installed in c:/my/site/mysite.

$ cd mysite

myname@myPC /my/site/mysite

$ jekyll serve

\# => Now browse to http://localhost:4000
</code>

If there is an error related to [liquid-exception](http://stackoverflow.com/questions/16498287/jekyll-liquid-exception-cannot-load-such-file-yajl-2-0-yajl) then add the following line in `_config.yml`

`highlighter: false`

Success will show this output:

Configuration file: c:/ae/aesite/_config.yml
            Source: c:/ae/aesite
       Destination: c:/ae/aesite/_site
      Generating...
                    done.
  Please add the following to your Gemfile to avoid polling for changes:
    require 'rbconfig'
    if RbConfig::CONFIG['target_os'] =~ /mswin|mingw|cygwin/i
      gem 'wdm', '>= 0.1.0'
    end
 Auto-regeneration: enabled for 'c:/my/site/mysite'
Configuration file: c:/my/site/mysite/_config.yml
    Server address: http://0.0.0.0:4000/
  Server running... press ctrl-c to stop.







