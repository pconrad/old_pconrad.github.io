# Setting up a local environment for Jekyll on Mac OS

This set of instructions explains how to set up a local environment for Jekyll on Mac OS.

I assume that you already know why you would want to do that.  If you are not sure, the 
[main README.md of this repo)[README.md] provides some context.

Here's an overview of the steps

1. Get git
1. Get homebrew
1. Get gpg
1. Get curl
1. Get ruby
1. Get ruby version manager (rvm)
1. Get bundler
1. Get jekyll

Now the details

# Get git

The best download site for git for Mac that I'm aware of is this one: https://git-scm.com/download/mac

If there is a better site, let me know.

I'm going to assume from here on out that you are comfortable with the git command line and with github.com

# Get ruby

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

# Get curl


Assuming that worked, we are now ready to install rvm.

# Get rvm

The installation instructions for rvm are here: https://rvm.io/rvm/install

As of 05/13/2016, they required you to first have pgp, which is why we already installed that above.




