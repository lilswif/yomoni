# Change log

This file contains al notable changes to the bertvv.httpd Ansible role.

This file adheres to the guidelines of [http://keepachangelog.com/](http://keepachangelog.com/). Versioning follows [Semantic Versioning](http://semver.org/).

## 1.2.0 - 2015-03-15

### Added

- Fedora support
- more SSL configuration options
- `httpd_ServerTokens` variable

## 1.1.0 - 2015-03-06

### Added

- Optional support for PHP

## 1.0.0 - 2015-03-06

First release!

### Added

- Install `httpd` and `mod_ssl` packages
- Configure Apache with template for `httpd.conf`
- Configure `mode_ssl` with template for `ssl.conf`
- Basic settings like port number, log file locations, and certificates can be customized


