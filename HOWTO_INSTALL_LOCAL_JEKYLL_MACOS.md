# Setting up a local environment for Jekyll on Mac OS

This set of instructions explains how to set up a local environment for Jekyll on Mac OS.

I assume that you already know why you would want to do that.  If you are not sure, the 
[main README.md of this repo)[README.md] provides some context.

Here's an overview of the steps

1. Get git
1. Make sure you have some version of Ruby (any version, for now)
1. Get homebrew
1. Get gpg
1. Get curl
1. Get ruby version manager (rvm)
1. Get ruby-2.1.7 
1. Get bundler
1. Get jekyll

Now the details

# Get git

The best download site for git for Mac that I'm aware of is this one: https://git-scm.com/download/mac

If there is a better site, let me know.

I'm going to assume from here on out that you are comfortable with the git command line and with github.com

# Make sure you have some version of Ruby (any version, for now)

You probably already have some version of ruby on your Mac OS X OS that came with it.   To find out, type

```
ruby --version
```

Output should be something like this:

```
169-231-85-67:~ pconrad$ ruby --version
ruby 2.3.0p0 (2015-12-25 revision 53290) [x86_64-darwin13]
169-231-85-67:~ pconrad$ 
```

If so, you are golden.  It doesn't matter what version of Ruby you have, 
because if you have pretty much any version of Ruby, you can use it to install `rvm`, 
which is the Ruby Version Manager.  
That will take care of all your Ruby versioning problems and installing of Ruby versions from now on.

But, first, we'll need to install homebrew if you don't have it already, so that we can install gpg if you don't have that already.  Sigh.

Fortunately, this is usually quick and painless.

# Get homebrew

The `homebrew` package manager lets you easily install/uninstall open source software on your Mac OS X system---typically packages that you might
normally expect to find on Unix-like systems, but that are not built into Mac OS X as delivered by Apple.

To install homebrew, visit: http://brew.sh/ and follow the instructions.  Note that you need ruby to do the install, so its a good thing we already did that!


# Get gpg

To install rvm, at least as of 05/13/2016, the first step required gpg.  

To see if it's installed, try this:

```
gpg --version
```

If you get `gpg: command not found`, here's how to install it with homebrew:


```
brew update
brew install gpg
```

Try the `gpg --version` command again to make sure it worked.

# Get curl

To install rvm, at least as of 05/13/2016, the second step required curl.  

To see if it's installed, try this:

```
curl --version
```

If you get `curl: command not found`, here's how to install it with homebrew:

```
brew update
brew install curl
```

Try the `curl --version` command again to make sure it worked.

Assuming that worked, we are now ready to install rvm.

# Get rvm

The installation instructions for rvm are here: https://rvm.io/rvm/install

As of 05/13/2016, they required you to first have gpg and curl, which is why we already installed those above.

Follow the instructions to install rvm

When you are done, type: 

```
rvm --version
```

You may get some instructions about modifying your dotfiles.   Hopefully, you know what the instructions are telling you to do, and why.    You'll need to follow those to get rvm to work properly.  It may help to know that what rvm does is manipulate your path to ensure that you are running the version of Ruby that you want to be running.

# Get ruby version 2.1.7

As of this writing, the Ruby version preferred for Jekyll on Github Pages is 2.1.7 (at least that's what I've been able to figure out).

So, you'll want to install that version of Ruby, and tell your shell that you want to use it. Here's how:

```
rvm install ruby-2.1.7
rvm use ruby-2.1.7
```

# Install bundler for this verison of ruby

Bundler is the thing that assembles all of your ruby "gems" (i.e resuable modules) into a bundle for your application.

You need the version of the bundler that goes with your current version of ruby.  To get it, do this:

```
gem install bundler
```

# Get jekyll

Then, to get jekyll, do this:

```
gem install jekyll
```
That installs the jekyll gem for this version of ruby.  You are now ready to try creating a Jekyll site.

To see if it worked, try this:

```
jekyll --version
```

If you got something like this, you are good:

```
169-231-85-67:try-jekyll pconrad$ jekyll --version
jekyll 3.1.3
169-231-85-67:try-jekyll pconrad$ 
```

Then, create and cd into an empty scratch directory (for now, it doesn't need to be a github repo---this is just for practice, and we are going to delete the files afterwards.)

In that empty directory, type this to create a jekyll site in the current directory: `jekyll new .`

That should look like this:

```
169-231-85-67:try-jekyll pconrad$ jekyll new .
New jekyll site installed in /Users/pconrad/try-jekyll. 
169-231-85-67:try-jekyll pconrad$ 
```

Afterwards, if you list your files, you'll see something like this:

```
169-231-85-67:try-jekyll pconrad$ ls
_config.yml	_layouts	_sass		css		index.html
_includes	_posts		about.md	feed.xml
169-231-85-67:try-jekyll pconrad$ 
```

Brief explanation of what you have here:

|  `_config.yml`       | jekyll configuration                     |
|----------------------|------------------------------------------|
|  `_posts`            | directory of md files containing content |

