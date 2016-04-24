# Puppet Module Demo

#### Table of Contents

1. [Overview](#overview)
2. [Module Description - What the module does and why it is useful](#module-description)
3. [Setup - The basics of getting started with demo](#setup)
    * [What demo affects](#what-demo-affects)
    * [Setup requirements](#setup-requirements)
    * [Beginning with demo](#beginning-with-demo)
4. [Usage - Configuration options and additional functionality](#usage)
5. [Reference - An under-the-hood peek at what the module is doing and how](#reference)
5. [Limitations - OS compatibility, etc.](#limitations)
6. [Development - Guide for contributing to the module](#development)

## Overview

This is a basic nordcloud puppet module skeleton. This README includes the required steps how to
get here fast and to start developing modules aligned with puppet best practice.


## Module Description

This section gives a brief description of the technology
the module integrates with and what that integration enables. This section
should answer the questions: "What does this module *do*?" and "Why would I use
it?"

#### Basic module class generator
Starting point is the [Puppetlabs module generator](https://docs.puppet.com/puppet/latest/reference/modules_publishing.html#build-your-module)
which sets up basic module class structure alongside rake tasks like syntax and rspec-puppet unit testing
making use of [puppetlabs_spec_helper](https://github.com/puppetlabs/puppetlabs_spec_helper).

#### Simple Puppet Module Structure Pattern
This module makes use of class ordering known as ["Simple Puppet Module Structure"](https://www.devco.net/archives/2012/12/13/simple-puppet-module-structure-redux.php)-Pattern.
which asumes the following runtime ordering:
```
 demo <- demo::service <- demo::configure <- demo::install
```
This brings logical ordering like: "install before configure" and "configure before start service" to the module
without introducing inter-module dependencies.

## Setup

### What demo affects

* A list of files, packages, services, or operations that the module will alter,
  impact, or execute on the system it's installed on.
* This is a great place to stick any warnings.
* Can be in list or paragraph form.

### Setup Requirements **OPTIONAL**

If your module requires anything extra before setting up (pluginsync enabled,
etc.), mention it here.

### Beginning with demo

The very basic steps needed for a user to get the module up and running.

This start with having puppet on a box running the following command:
``` sh
~/$ puppet module generate nordcloud-demo
```
This generates us the module skeleton nodcloud-demo:
```
~/$ ls -al  nordcloud-demo
insgesamt 60
drwxrwxr-x 7 xxx xxx 4096 Apr 24 20:08 .
drwxrwxr-x 8 xxx xxx 4096 Apr 24 19:31 ..
-rw-r--r-- 1 xxx xxx  242 Apr 24 19:31 Gemfile
-rw-rw-r-- 1 xxx xxx 1083 Apr 24 19:34 LICENSE
drwxrwxr-x 2 xxx xxx 4096 Apr 24 19:31 manifests
-rw-rw-r-- 1 xxx xxx  441 Apr 24 19:31 metadata.json
-rw-r--r-- 1 xxx xxx  633 Apr 24 19:31 Rakefile
-rw-rw-r-- 1 xxx xxx 3205 Apr 24 20:08 README.md
drwxrwxr-x 4 xxx xxx 4096 Apr 24 19:40 spec
drwxrwxr-x 2 xxx xxx 4096 Apr 24 19:31 tests

```



If your most recent release breaks compatibility or requires particular steps
for upgrading, you may wish to include an additional section here: Upgrading
(For an example, see http://forge.puppetlabs.com/puppetlabs/firewall).

## Usage

Put the classes, types, and resources for customizing, configuring, and doing
the fancy stuff with your module here.

## Reference

Here, list the classes, types, providers, facts, etc contained in your module.
This section should include all of the under-the-hood workings of your module so
people know what the module is touching on their system but don't need to mess
with things. (We are working on automating this section!)

## Limitations

This is where you list OS compatibility, version compatibility, etc.

## Development

Since your module is awesome, other users will want to play with it. Let them
know what the ground rules for contributing are.

## Release Notes/Contributors/Etc **Optional**

If you aren't using changelog, put your release notes here (though you should
consider using changelog). You may also add any additional sections you feel are
necessary or important to include here. Please use the `## ` header.
