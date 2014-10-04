# Setup Octoless on Windows
```
    where less===more && !sass<y
```

The setup requires creating multiple forks of a GitHub repo and good instructions can be found here:
[http://adrianshort.org/create-multiple-forks-of-a-github-repo/](http://adrianshort.org/create-multiple-forks-of-a-github-repo/)

Octoless is a fork of a fork of Octopress.

If an error message like this is seen when pushing to master:

```
hint: Updates were rejected because the remote contains work that you do
not have locally...
```

it indicates something different exists in the new repo. The most likely
cause is adding a README.MD or other file on the github repo so that it is
no longer in sync with the local version.

This can be resolved with the command:

```
$ git push -f -u origin master
```

to force the update.

## Install Required Software

[Detailed docs are here](http://octopress.org/docs/)

[Install git](http://git-scm.com/)

```
$ git --version
git version 1.9.4.msysgit.2
```

[Install Ruby](http://rubyinstaller.org/)

```
$ ruby --version
ruby 2.1.3p242 (2014-09-19 revision 47630) [i386-mingw32]
```

Run git bash and try the command `ruby --version`

If it reports *command not found* then fix the windows path environment variable as follows:

Right click My Computer, click Properties, go to the Advanced tab, click on Environmental Variables below, go to System Variables below, select Path, click Edit and in the beginning of the path enter: `C:\Ruby21-x64;`

Adjust the ruby path as needed according to the version that was installed.

### Install Dependencies

`$ gem install bundler`

<code>
Fetching: bundler-1.7.3.gem (100%)

Successfully installed bundler-1.7.3

Parsing documentation for bundler-1.7.3

Installing ri documentation for bundler-1.7.3

Done installing documentation for bundler after 14 seconds

1 gem installed
</code>

Download the appropriate [DevKit](http://rubyinstaller.org/downloads) and review detailed instructions 
at [http://github.com/oneclick/rubyinstaller/wiki/Development-Kit](http://github.com/oneclick/rubyinstaller/wiki/Development-Kit)

Install to: `C:\RubyDK` then

`$ cd /c/rubydk`

`$ ruby dk.rb init`

<code>
[INFO] found RubyInstaller v2.1.3 at C:/Ruby21

Initialization complete! Please review and modify the auto-generated
'config.yml' file to ensure it contains the root directories to all
of the installed Rubies you want enhanced by the DevKit.
</code>

`ruby dk.rb install`

<code>
[INFO] Updating convenience notice gem override for 'C:/Ruby21'

[INFO] Installing 'C:/Ruby21/lib/ruby/site_ruby/devkit.rb'
</code>

Change back to the correct location of the *octoless* folder and install the appropriate bundles:

`$ cd octoless`

`$ bundle install`

This will install **lots of gems** and finish with:

<code>
Your bundle is complete!

Use bundle show [gemname] to see where a bundled gem is installed.

Post-install message from haml:

HEADS UP! Haml 4.0 has many improvements, but also has changes that may break 
your application:

*Support for Ruby 1.8.6 dropped

*Support for Rails 2 dropped

*Sass filter now always outputs < style> tags

*Data attributes are now hyphenated, not underscored

*html2haml utility moved to the html2haml gem

*Textile and Maruku filters moved to the haml-contrib gem

For more info see:

http://rubydoc.info/github/haml/haml/file/CHANGELOG.md
</code>

### Install Default Octopress Theme

`$ rake install`

This command shows the following ouput:

`## Set the codepage to 65001 for Windows machines`

`## Copying classic theme into ./source and ./sass`

`mkdir -p source`

`cp -r .themes/classic/source/. source`

`mkdir -p sass`

`cp -r .themes/classic/sass/. sass`

`mkdir -p source/_posts`

`mkdir -p public`

This is what `rake install` does behind the scenes:

* create a source/ folder
* copy default theme's source into source/
* create a sass/ folder
* copy the default theme's sass into sass/
* create a _posts folder under source/
* create a public/ folder

### Test Installation

Confirm your Ruby environment is correctly using the DevKit by running

`$ gem install json --platform=ruby`

JSON should install correctly and you should see `Building native extensions`  in the screen messages. Next run

`$ ruby -rubygems -e "require 'json'; puts JSON.load('[42]').inspect"`

to confirm that the json gem is working.

# Deploying to Github Pages

Create a new Github repository and name the repository with the format `username.github.io`, where username is your GitHub user name or organization name.

Github Pages for users and organizations uses the master branch like the public directory on a web server, serving up the files at your Pages url `http://username.github.io`. As a result, you should work on the source for your blog in the source branch and *commit the generated content* to the **master** branch. Octoless has a configuration command to help set this up:

## Configure Global Variables

Configure the site  global variables such as site name, site link, username etc. This is done by editing the `_config.yml` file.

* url: The url of generated github pages e.g. http://the_username.github.io/the_repo_name
* title: The site title.
* subtitle: The site subtitle
* author: Real Name

## Connect Local Source to the GitHub Repo

Octoless generates static page assets and pushes to the [GitHub Pages](https://pages.github.com/) branch of the repo.

`$ rake setup_github_pages`

<code>
\## Set the codepage to 65001 for Windows machines

Enter the read/write url for your repository
(For example, 'git@github.com:your_username/your_username.github.io.git)

           or 'https://github.com/your_username/your_username.github.io')

Repository url: https://github.com/my_site/my_site.github.io

rm -rf _deploy

mkdir _deploy

cd _deploy

Initialized empty Git repository in c:/some_location/octoless/_deploy/.git/

warning: CRLF will be replaced by LF in index.html.

The file will have its original line endings in your working directory.

[master (root-commit) 1598ac9] Octoless init

warning: CRLF will be replaced by LF in index.html.

The file will have its original line endings in your working directory.

1 file changed, 1 insertion(+)

create mode 100644 index.html

cd -

\## Now you can deploy to https://github.com/my_site/my_site.github.io with `rake d
eploy` ##
</code>

## Generate Some Static Assets

Generate necessary assets and deploy to gh-pages branch. This work is automated with the built-in Octoless rake tasks.






