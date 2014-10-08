# Hyde Away

My Installation of Jekyll on Windows 8.1 x32

Requirements:

- Install Git Bash

- Install Ruby

- Install Ruby Development Kit

- Install RubyGems

- Install Jekyll

---

## Installation of Requirements

### Install Git Bash

### Install Ruby

### Install Ruby Development Kit

Download the appropriate [DevKit](http://rubyinstaller.org/downloads) and review detailed instructions 
at [http://github.com/oneclick/rubyinstaller/wiki/Development-Kit](http://github.com/oneclick/rubyinstaller/wiki/Development-Kit)

Install to: `C:\RubyDK` then

<code>
$ cd /c/rubydk

$ ruby dk.rb init

[INFO] found RubyInstaller v2.1.3 at C:/Ruby21

Initialization complete! Please review and modify the auto-generated 'config.yml' file to ensure it contains the root directories to all of the installed Rubies you want enhanced by the DevKit.
</code>

Bind the devkit to ruby installations in your path:

<code>
$ ruby dk.rb install

[INFO] Updating convenience notice gem override for 'C:/Ruby21'

[INFO] Installing 'C:/Ruby21/lib/ruby/site_ruby/devkit.rb'
</code>

### Install Update for RubyGems

<code>
$ gem update --system

...

RubyGems system software updated
</code>

### Install Jekyll

<code>
$ gem install jekyll

...

Fetching: jekyll-2.4.0.gem (100%)

Successfully installed jekyll-2.4.0

...

Parsing documentation for jekyll-2.4.0

Installing ri documentation for jekyll-2.4.0

...

Done installing documentation for blankslate, celluloid, classifier-reborn, coff
ee-script, coffee-script-source, execjs, fast-stemmer, ffi, hitimes, jekyll, jek
yll-coffeescript, jekyll-gist, jekyll-paginate, jekyll-sass-converter, jekyll-wa
tch, listen, parslet, posix-spawn, pygments.rb, rb-fsevent, rb-inotify, redcarpe
t, sass, timers, toml, yajl-ruby after 68 seconds

26 gems installed
</code>

## Verify Installation

Here

### Bash

<code>
myname@ myPC /c/my/site

$ bash

bash-3.1$

GNU bash, version 3.1.20(4)-release (i686-pc-msys)
</code>

Use Ctrl-D to exit GNU bash

### Ruby and Git

<code>
$ ruby --version

ruby 2.1.3p242 (2014-09-19 revision 47630) [i386-mingw32]

$ git --version

git version 1.9.4.msysgit.2
</code>

### Jekyll 

<code>
$ gem query jekyll

\*\*\* LOCAL GEMS \*\*\*

jekyll (2.4.0)

jekyll-coffeescript (1.0.1)

jekyll-gist (1.1.0)

jekyll-paginate (1.0.0)

jekyll-sass-converter (1.2.1)

jekyll-watch (1.1.1)
</code>

# Create Jekyll Site

<code>
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

<code>
Configuration file: c:/my/site/mysite/_config.yml

Source: c:/my/site/mysite

Destination: c:/my/site/mysite/_site

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
</code>

## Add Site to GitHub

Follow the [git command line instructions](https://help.github.com/articles/adding-an-existing-project-to-github-using-the-command-line/) to add the site as a repo on GitHub.

The bash console will now display:

<code>
myname@myPC /c/my/site/mysite (master)

$
</code>

# Configuration

Edit the file `_config.yml` to required settings for the site configuration, such as timezone. Detailed information is provided [here](http://jekyllrb.com/docs/configuration/) for available options.








