============================================
vbotka.freebsd_postinstall 2.6 Release Notes
============================================

.. contents:: Topics


2.6.12
======

Release Summary
---------------
Feature and bugfix release with docs update.

Major changes
-------------
* Support 14.1

Minor Changes
-------------
* Bump docs version.
* Update hosts sanity testing.
* Update passwords.


2.6.11
======

Release Summary
---------------
Feature and docs update.

Major changes
-------------
* Support 13.3 and 14.0

Minor Changes
-------------
* Formatting Travis config.
* Update Ansible lint config.
* Update README
* Exclude docs from local ansible-lint
* Use default rules in local ansible-lint
* Update docs.


2.6.10
======

Release Summary
---------------
Fix test.


2.6.9
=====

Release Summary
---------------
Update defaults/pkgdict_*, freebsd-update, and tests.

Major changes
-------------

Minor Changes
-------------
* Add ports-mgmt/portsnap to defaults/pkgdict_*
* Update freebsd-update. Do not require installation of jc.
* Update tests.


2.6.8
=====

Release Summary
---------------
Update docs requirements readthedocs-sphinx-search==0.3.2


2.6.7
=====

Release Summary
---------------
Feature update and fixes.

Major changes
-------------
* Add tasks vars.yml. Add variables fp_vars(d=false),
  fp_vars_default_versions(d=false), and fp_vars_debug(d:false).
  Get default versions from /usr/ports/Mk/bsd.default-versions.mk
  Creates dictionary pf_default_versions.
* Update defaults/main/pkgdict_versions.yml. Use pf_default_versions
  if avaialable.
* Update defaults/main/pkgdict_*.yml
* Add bsd_gcc_version, bsd_gcc_version_default, and bsd_make_gcc_version
* Add bsd_ssl_version, bsd_ssl_version_default, and bsd_make_ssl_version
* Update tasks/packages.yml and packages-install.yml
* Update vars/samples/make.yml.sample
* Update vars/samples/packages.yml.sample

Minor Changes
-------------
* Update docs
* Update vars debug label.

Bugfixes
--------

Breaking Changes / Porting Guide
--------------------------------
* Update defaults/main/pkgdict_*.yml; Use bsd_gcc_version; Split
  pkglist pip from devel.

2.6.6
=====

Release Summary
---------------
Update to Ansible 2.16. Add FreeBSD 14.0

Major changes
-------------
* Add support to manage /etc/freebsd-update.conf
* Add support to manage inetd, /etc/hosts.allow
* Add support to manage syslogd
* Update smartd, apcupsd, devfs, hostapd, nfsd, nfs, ntpdate, ntp,
  qemu, resolvconf, snmpd, sshd, swap, sysctl, wpasupplicant
* Update procmail. Configure /usr/local/etc/procmailrc
* Add variables bsd_perl_version, bsd_make_perl_version.
  Add vars/samples/make.yml.sample

Minor Changes
-------------
* Update docs

Bugfixes
--------
* #4 Fix apcupsd script location
* #4 Remove double quote when using ntpdate rc vars

Breaking Changes / Porting Guide
--------------------------------
* Update defaults/main/pkgdict_versions.yml


2.6.5
=====

Release Summary
---------------
Fix requirements: docs/requirements.txt


2.6.4
=====

Release Summary
---------------
Update fstab. Add changelog. Add docs/requirements.txt

Major changes
-------------
* Formatting and comments in swap.
* Configure fstab swap entries.
* Update fstab sample vars.
* Add ansible_python_version to debug.


2.6.3
=====

Release Summary
---------------
Fix updates

Major changes
-------------
* Added RTD conf file.
* Run groupwrappers before groups.


2.6.2
=====

Release Summary
---------------
Update Ansible 2.14, meta, license

Minor changes
-------------
* Update debug formatting
* Update docs debug
* Update docs themes


2.6.1
=====

Release Summary
---------------
Format debug output, tags, and defaults

Minor changes
-------------
* Format and fix fp_sanity_tags
* Format debug output
* Split vars/main.yml.sample and put samples into the vars/samples
* Update docs


2.6.0
=====

Release Summary
---------------
Add dhclient. Updated docs

Major Changes
-------------

Minor Changes
-------------

Bugfixes
--------

Breaking Changes / Porting Guide
--------------------------------
