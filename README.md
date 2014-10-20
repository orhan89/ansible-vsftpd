# Ansible Vsftpd Role

[![Build Status](https://travis-ci.org/weareinteractive/ansible-vsftpd.png?branch=master)](https://travis-ci.org/weareinteractive/ansible-vsftpd)
[![Stories in Ready](https://badge.waffle.io/weareinteractive/ansible-vsftpd.svg?label=ready&title=Ready)](http://waffle.io/weareinteractive/ansible-vsftpd)

> `vsftpd` is an [ansible](http://www.ansible.com) role which: 
> 
> * installs vsftpd
> * configures vsftpd


## Installation

Using `ansible-galaxy`:

```
$ ansible-galaxy install franklinkim.vsftpd
```

Using `arm` ([Ansible Role Manager](https://github.com/mirskytech/ansible-role-manager/)):

```
$ arm install franklinkim.vsftpd
```

Using `git`:

```
$ git clone https://github.com/weareinteractive/ansible-vsftpd.git
```

## Variables

Here is a list of all the default variables for this role, which are also available in `defaults/main.yml`.

```
# vsftpd_config:
#   local_umask: 022
#

# config variables
vsftpd_config: {}
# config template to install, relative to the ansible repository root
vsftpd_config_template:
```

## Handlers

These are the handlers that are defined in `handlers/main.yml`.

* `restart vsftpd` 

## Example playbook

```
- host: all
  sudo: yes
  roles: 
    - franklinkim.vsftpd
  vars:
```

## Testing

```
$ git clone https://github.com/weareinteractive/ansible-vsftpd.git
$ cd ansible-vsftpd
$ vagrant up
```

## Roadmap

* provide sftp
* use franklinkim.users

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests and examples for any new or changed functionality.

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## License
Copyright (c) We Are Interactive under the MIT license.
