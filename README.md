-*- mode: markdown; mode: visual-line;  -*-

# Debmirror Puppet Module 

[![Puppet Forge](http://img.shields.io/puppetforge/v/ULHPC/debmirror.svg)](https://forge.puppetlabs.com/ULHPC/debmirror)
[![License](http://img.shields.io/:license-GPL3.0-blue.svg)](LICENSE)
![Supported Platforms](http://img.shields.io/badge/platform-debian-lightgrey.svg)
[![Documentation Status](https://readthedocs.org/projects/ulhpc-puppet-debmirror/badge/?version=latest)](https://readthedocs.org/projects/ulhpc-puppet-debmirror/?badge=latest)

Configure and manage Debian mirrors

      Copyright (c) 2015 S. Varrette, H. Cartiaux, V. Plugaru, S. Diehl aka. UL HPC Management Team <hpc-sysadmins@uni.lu>
      

| [Project Page](https://github.com/ULHPC/puppet-debmirror) | [Sources](https://github.com/ULHPC/puppet-debmirror) | [Documentation](https://ulhpc-puppet-debmirror.readthedocs.org/en/latest/) | [Issues](https://github.com/ULHPC/puppet-debmirror/issues) |

## Synopsis

Configure and manage Debian mirrors.

This module implements the following elements: 

* __Puppet classes__:

* __Puppet definitions__: 

All these components are configured through a set of variables you will find in
[`manifests/params.pp`](manifests/params.pp). 

_Note_: the various operations that can be conducted from this repository are piloted from a [`Rakefile`](https://github.com/ruby/rake) and assumes you have a running [Ruby](https://www.ruby-lang.org/en/) installation.
See `docs/contributing.md` for more details on the steps you shall follow to have this `Rakefile` working properly. 

## Dependencies

See [`metadata.json`](metadata.json). In particular, this module depends on 

* [puppetlabs/stdlib](https://forge.puppetlabs.com/puppetlabs/stdlib)
* [puppetlabs/vcsrepo](https://forge.puppetlabs.com/puppetlabs/vcsrepo)
* [ULHPC/nfs](https://forge.puppetlabs.com/ULHPC/nfs)

## Overview and Usage

### Class `debmirror`

This is the main class defined in this module.
It accepts the following parameters: 

* `$ensure`: default to 'present', can be 'absent'

Use it as follows:

     include ' debmirror'

See also [`tests/init.pp`](tests/init.pp)



## Librarian-Puppet / R10K Setup

You can of course configure the debmirror module in your `Puppetfile` to make it available with [Librarian puppet](http://librarian-puppet.com/) or
[r10k](https://github.com/adrienthebo/r10k) by adding the following entry:

     # Modules from the Puppet Forge
     mod "ULHPC-debmirror"

or, if you prefer to work on the git version: 

     mod "ULHPC-debmirror", 
         :git => 'https://github.com/ULHPC/puppet-debmirror',
         :ref => 'production' 

## Issues / Feature request

You can submit bug / issues / feature request using the [ULHPC-debmirror Puppet Module Tracker](https://github.com/ULHPC/puppet-debmirror/issues). 

## Developments / Contributing to the code 

If you want to contribute to the code, you shall be aware of the way this module is organized. 
These elements are detailed on [`docs/contributing.md`](contributing/index.md).

You are more than welcome to contribute to its development by [sending a pull request](https://help.github.com/articles/using-pull-requests). 

## Puppet modules tests within a Vagrant box

The best way to test this module in a non-intrusive way is to rely on [Vagrant](http://www.vagrantup.com/).
The `Vagrantfile` at the root of the repository pilot the provisioning various vagrant boxes available on [Vagrant cloud](https://atlas.hashicorp.com/boxes/search?utf8=%E2%9C%93&sort=&provider=virtualbox&q=svarrette) you can use to test this module.

See [`docs/vagrant.md`](vagrant.md) for more details. 

## Online Documentation

[Read the Docs](https://readthedocs.org/) aka RTFD hosts documentation for the open source community and the [ULHPC-debmirror](https://github.com/ULHPC/puppet-debmirror) puppet module has its documentation (see the `docs/` directly) hosted on [readthedocs](http://ulhpc-puppet-debmirror.rtfd.org).

See [`docs/rtfd.md`](rtfd.md) for more details.

## Licence

This project and the sources proposed within this repository are released under the terms of the [GPL-3.0](LICENCE) licence.


[![Licence](https://www.gnu.org/graphics/gplv3-88x31.png)](LICENSE)
