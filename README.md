# pconrad.github.io

This is the github repo for the website pconrad.github.io, which is hosted by Github Pages, and produced using software called Jekyll.

Jekyll is a "blog-aware Ruby-based static site generator".  It isn't exactly a "content management system", but it has some aspects of one.   The best part is that there is no "database" to configure: all of the content is stored in static files kept in a github repository (this one).   And the web hosting provider is Github itself.

This has many benefits:

* If I want to make a change, I just edit the content, either editing/creating/uploading files directly through the github.com web interface, or by cloning the repo, editing locally, and using "git push" to update this repo.
* Every time the repo is updated with a push, the website is rebuilt by the Jekyll software.
* I can set up Continuous Integration on TravisCI so that I can look at "log files" to see if/when there are build errors.
* The authentication is exactly the same as the authentication for this github repo. If I want to give someone edit access, I just make them a collaborator on this repo.  They use their github credentials to log in and change content.

In this README.md, I am documenting for myself and for others, the process by which this is all set up.

# Step 1: Create a repo with the correct name

My understanding is that you can publish a website via a gh-pages branch of any github repo.   But the *easiest* path is to use the following naming convention--if you do, then you don't need to worry about any branch other than the master branch:

* For a personal github account, e.g. pconrad, the repo should be named EXACTLY pconrad.github.io, and should be stored under github.com/pconrad/pconrad.github.io    That naming convention automatically triggers that you are hosting a personal page stored under Github Pages.

* For an organization github account, e.g. an organization associated with a course such as UCSB-CS56-M16:
 * the repo should be named UCSB-CS56-M16.github.io 
 * it should be stored under github.com/UCSB-CS56-M16/UCSB-CS56-M16.github.io 
 * This automatically triggers that you are hosting an organization page
 
# Step 2: Do you really want Jekyll?

If you want to keep things simple, at this point you could just put an index.html, site.css etc. in the repo and be done with it.

That will make an easy peasy web site.

So, decide at this point, whether you really need the extra bells and whistles you get with Jekyll, such as automatic indexing of pages, common headers/footers, etc.

If you do, then continue.


# Step 3: Optional, but recommended: configure a local environment for Jekyll.

What is this step all about? It's about configuring a local environment on your own computer (my instructions are tailored for Mac OS X) that allows you to run a local instance of Jekyll on your own machine as a test environment.  This allows you to check, quickly, whether everything is working, before deploying changes to the server.  It is often easier to see in a local environment what is wrong that it is to see in the "cloud".

What makes this step a bit onerous is that to really make things work properly, you need, in addition to git, which we assume you already have, all of the following:
| Ruby | Ruby Version Manager (rvm) | Bundler | jekyll  |
|------|----------------------------|---------|---------|
|      |                            |         |         |

However, since this step is a bit onerous, and isn't strictly necessary, I've factored it out into its own .md file: [HOWTO_INSTALL_LOCAL_JEKYLL_MACOS.md](HOWTO_INSTALL_LOCAL_JEKYLL_MACOS.md).


Once you've either done that, or not, you may proceed to the next step.

