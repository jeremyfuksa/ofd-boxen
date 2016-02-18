# This file manages Puppet module dependencies.
#
# It works a lot like Bundler. We provide some core modules by
# default. This ensures at least the ability to construct a basic
# environment.

# Shortcut for a module from GitHub's boxen organization
def github(name, *args)
  options ||= if args.last.is_a? Hash
    args.last
  else
    {}
  end

  if path = options.delete(:path)
    mod name, :path => path
  else
    version = args.first
    options[:repo] ||= "boxen/puppet-#{name}"
    mod name, version, :github_tarball => options[:repo]
  end
end

# Shortcut for a module under development
def dev(name, *args)
  mod "puppet-#{name}", :path => "#{ENV['HOME']}/src/boxen/puppet-#{name}"
end

# githubs many of our custom types and providers, as well as global
# config. Required.

github "boxen", "3.11.1"

# Support for default hiera data in modules

github "module_data", "0.0.4", :repo => "ripienaar/puppet-module-data"

# Core modules for a basic development environment. You can replace
# some/most of these if you want, but it's not recommended.

github "brewcask",    "0.0.6"
github "foreman",     "1.2.0"
github "gcc",         "3.0.2"
github "git",         "2.7.92"
github "homebrew",    "1.13.0"
github "inifile",     "1.4.1", :repo => "puppetlabs/puppetlabs-inifile"
github "nodejs",      "5.6.0"
github "openssl",     "1.0.0"
github "phantomjs",   "3.0.0"
github "pkgconfig",   "1.0.0"
github "repository",  "2.4.1"
github "ruby",        "8.5.4"
github "stdlib",      "4.7.0", :repo => "puppetlabs/puppetlabs-stdlib"
github "sudo",        "1.0.0"
github "xquartz",     "1.2.1"

github "adobe_creative_cloud", :repo => "ngs/puppet-adobe_creative_cloud"
github "iterm2", "1.0.0", :repo => "boxen/puppet-iterm2"
github "chrome"
github "dropbox"
github "mysql"
github "onepassword"
github "virtualbox"
github "vagrant"
github "heroku"
github "arduino"
github "skype"
github "tower"
github "omnigraffle"
github "spotify"
github "slack"
github "lingon"
github "bartender"
github "transmit"
github "transmission"
github "things"
github "sequel_pro"
github "postbox"
github "handbrake"
github "caffeine"
github "harvest"
github "googledrive"
github "imageoptim"
github "osx"
github "atom"
github "php"

# Optional/custom modules. There are tons available at
# https://github.com/boxen.
# github "elasticsearch", "2.8.0"
# github "mysql",         "2.0.1"
# github "postgresql",  "4.0.1"
# github "redis",       "3.1.0"
# github "sysctl",      "1.0.1"
