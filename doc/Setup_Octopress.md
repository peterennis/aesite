#Setup Octopress on Windows

##Install Required Software

[Detailed docs are here](http://octopress.org/docs/)

[Install git](http://git-scm.com/)

[Install Ruby](http://rubyinstaller.org/)

Run git bash and try the command `ruby --version`

If it reports *command not found* then fix the windows path environment variable as follows:

Right click My Computer, click Properties, go to the Advanced tab, click on Environmental Variables below, go to System Variables below, select Path, click Edit and in the beginning of the path enter: `C:\Ruby21-x64;`

Adjust the ruby path as needed according to the version that was installed. The output should be similar to this:

`$ ruby --version`

`ruby 2.1.3p242 (2014-09-19 revision 47630) [x64-mingw32]`

##Clone Octopress

The following commands in git bash will clone Octopress into a folder *octopress* where you are currently located, and then change to the new folder.

`$ git clone git://github.com/imathis/octopress.git octopress`

`cd octopress`

###Install Dependencies

`$ gem install bundler`

Download the appropriate [DevKit](http://rubyinstaller.org/downloads) and review detailed instructions 
at [http://github.com/oneclick/rubyinstaller/wiki/Development-Kit](http://github.com/oneclick/rubyinstaller/wiki/Development-Kit')

Install to: `C:\rubydk` then

`$ cd /c/rubydk`

`$ ruby dk.rb init`

`[INFO] found RubyInstaller v2.1.3 at C:/Ruby21-x64`

`Initialization complete! Please review and modify the auto-generated`
`'config.yml' file to ensure it contains the root directories to all`
`of the installed Rubies you want enhanced by the DevKit.`

`$ ruby dk.rb install`

`[INFO] Updating convenience notice gem override for 'C:/Ruby21-x64'`

`[INFO] Installing 'C:/Ruby21-x64/lib/ruby/site_ruby/devkit.rb'`

Change back to the correct location of the *octopress* folder and install the appropriate bundles:

`$ cd octopress`

`$ bundle install`

This will install **lots of gems** and finish with:

`Your bundle is complete!`

`Use bundle show [gemname] to see where a bundled gem is installed.`

`Post-install message from haml:`

`HEADS UP! Haml 4.0 has many improvements, but also has changes that may break`

`your application:`

`* Support for Ruby 1.8.6 dropped`

`* Support for Rails 2 dropped`

`* Sass filter now always outputs <style> tags`

`* Data attributes are now hyphenated, not underscored`

`* html2haml utility moved to the html2haml gem`

`* Textile and Maruku filters moved to the haml-contrib gem`

`For more info see:`

`http://rubydoc.info/github/haml/haml/file/CHANGELOG.md`

###Install Default Octopress Theme

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

#Deploying to Github Pages

Create a new Github repository and name the repository with the format `username.github.io`, where username is your GitHub user name or organization name.

Github Pages for users and organizations uses the master branch like the public directory on a web server, serving up the files at your Pages url `http://username.github.io`. As a result, you'll want to work on the source for your blog in the source branch and *commit the generated content* to the **master** branch. Octopress has a configuration command to help set this up:

`$ rake setup_github_pages`

`## Set the codepage to 65001 for Windows machines`

`Enter the read/write url for your repository`

`(For example, 'git@github.com:your_username/your_username.github.io.git)`

`           or 'https://github.com/your_username/your_username.github.io')`

`Repository url:`

Fill in your details.

`Repository url: https://github.com/.../...github.io`

`Added remote https://github.com/.../...github.io as origin`

`Set origin as default remote`

`Master branch renamed to 'source' for committing your blog source files`

`rm -rf _deploy`

`mkdir _deploy`

`cd _deploy`

`Initialized empty Git repository in .../octopress/_deploy/.git/`

`'My Octopress Page is coming soon`

If you see ['hellip' is not recognized as an internal or external command](http://derantell.github.io/blog/2012/12/02/getting-started-with-octopress-on-windows/) then follow the link for a good solution. You have to edit `rakefile` and replace *&hellip* with something else.

`[master (root-commit) 411adf7] Octopress init`

` 1 file changed, 0 insertions(+), 0 deletions(-)`

` create mode 100644 index.html`

`cd -`

`---`

`## Now you can deploy to https://github.com/.../...github.io`

` with rake deploy ##`

##Generate the Site

`$ rake generate`

`## Set the codepage to 65001 for Windows machines`

`## Generating Site with Jekyll`

`directory source/stylesheets/`

`create source/stylesheets/screen.css`

`Configuration file: c:/ae/octopress/_config.yml`

`Source: source`

`Destination: public`

`Generating...`

`done.`

`Auto-regeneration: disabled. Use --watch to enable.`
 
## Deploy the Site

`$ rake deploy`

This will install **lots of gems** and finish with:

`## Pushing generated _deploy website`

`Username for 'https://github.com':`

The site will now deploy. If you see this message:

` ! [rejected]        master -> master (non-fast-forward)`

then something exists on your remote site. Do a pull and
merge any conflicts then deploy again.

A successful deploy will complete with a report similar to this:

`Counting objects: 82, done.`

`Delta compression using up to 8 threads.`

`Compressing objects: 100% (73/73), done.`

`Writing objects: 100% (80/80), 186.67 KiB | 0 bytes/s, done.`

`Total 80 (delta 2), reused 0 (delta 0)`

`To https://github.com/.../...github.io.git`

`   1f9299a..13ea0ec  master -> master`

`## Github Pages deploy complete`

`cd -`


