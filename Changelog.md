# Changelog

## 15.3.3

### New

* New brand for mesh.io. [Tobias Schäfer]

### Changes

* Simplified and unified the README file. [Tobias Schäfer]
* Simplified manifest medata key descriptions. [Tobias Schäfer]

## 15.3.2

### Fix

* Allow IPv6 statless addrconf. Removed ndpd config file. [Tobias Schäfer]

## 15.3.1

### New

* Nagios NRPE will help to monitor our zones even better. [Tobias Schäfer]

## 15.3.0

### New

* Update to new version 15.3.0 [Tobias Schäfer]

  Use new minimal base image from joyent and latest pkgsrc release.
  Update manifest to new version.

### Fix

* Complete mdata description in manifest JSON file. [Tobias Schäfer]
* Adapt README. [Tobias Schäfer]

## 15.1.3

### New

* We also need findutils for gnufind. [Thomas Merkel]

## 15.1.2

### Fix

* We require coreutils for many script on our system so we install that by default. [Thomas Merkel]

## 15.1.1

### New

* Sudo is required on many images. [Thomas Merkel]
* Install base64 as default tool and also add znapzend as default backup tool. [Thomas Merkel]

## 15.1.0

### New

* Update to new version 15.1.0. [Thomas Merkel]

  Use new minimal base image from joyent. Be sure we're using pkgsrc nullmailer
  version. Update manifests to new version.

## 14.4.2

### Fix

* Script for ssh host key setup. [Thomas Merkel]

  The script only should run once and disable itself. It should also be not
  enabled by default and should be started by an extra mdata / zoneinit script.

### Changes

* Version bump because of minimal change. [Thomas Merkel]
* The core smf should be started before other core scripts run. [Thomas Merkel]

## 14.4.1

### New

* Add own wrapper for our personal SMF scripts which should be included / imported. [Thomas Merkel]
* Add manifest and method for storing ssh keys in mdata variable. [Thomas Merkel]
* We create an extra sshd host key mdata script. [Thomas Merkel]

### Changes

* Switch to own rsyslog config for the future. [Thomas Merkel]
* Rename / copy the rsyslog config from system to pkgsrc. [Thomas Merkel]
* Disable systemlog and use pkgsrc rsyslog version. [Thomas Merkel]

  We would like to have gnutls for rsyslog. So we disable system
  log which is also rsyslog and install the new rsyslog version
  including gnutls module.

### Other

* We would like to use the minimal version for base image. [Thomas Merkel]
* Update to newest 14.4.1 base. [Thomas Merkel]

## 14.4.0

### New

* Version update to 14.4.0 release. [Thomas Merkel]

	This patch is created by @wiedi. We switch from postfix to nullmailer.
	By default the new minimal base image didn't contain any mailing
	daemon so we remove the postfix configuration scripts and replace them
	with an nullmailer setup.

* Our own packages are signed with pkgsrc@skylime.net GPG key. [Thomas Merkel]

	We replace the current keyring with a new one which contains the
	public key from Joyent and from SkyLime

### Changes

* Set hostname for nullmailer smtp out. [Thomas Merkel]
* Enable nullmailer by default if smarthost exists. [Thomas Merkel]
* update pkgsrc version. [Thomas Merkel]
* Modify to use the new script to generate the munin plugins. [Thomas Merkel]

### Other

* remove debug output. [Thomas Merkel]
* Allow also env variables for PLUGINS. [Thomas Merkel]
* Add first version of munin-node-plugins script. [Thomas Merkel]
* release of new munin plugins (support more dovecot logs) [Thomas Merkel]
* add tool ccze for colored log output. [Thomas Merkel]

## 14.2.9

### Changes

* update changelog. [Thomas Merkel]
* version update for last patches. [Thomas Merkel]

### Other

* version bump. [Thomas Merkel]
* update smartos munin plugins. [Thomas Merkel]
* Enable svc service by email. [Thomas Merkel]

## 14.2.8

### Changes

* version update for last patches. [Thomas Merkel]

### Other

* Enable svc service by email. [Thomas Merkel]

## 14.2.7 (2014-10-07)

### New

* version bump for mibe image. [Thomas Merkel]
* add ssh private key mdata option for root user. [Thomas Merkel]

    We would like to store the public and private ssh key for the root
    user in mdata. This allow us to have that information after
    reprovision a zone. The only valid key must be an rsa key and the
    public key ist mostly not required by the system.

* add logtail with the pkg logcheck. [Thomas Merkel]

### Changes

* update changelog file. [Thomas Merkel]
* update to new munin scripts. [Thomas Merkel]

## 14.2.6 (2014-10-06)

### New

* add dtracetools for debugging to base update version number. [Thomas Merkel]
* add dtracetools for debugging to base. [Thomas Merkel]

### Changes

* update changelog. [Thomas Merkel]

## 14.2.5 (2014-10-02)

### New

* version update. [Thomas Merkel]
* add leading number to the rsyslog remote log config file. [Thomas Merkel]
* add additional default configuration for rsyslog. [Thomas Merkel]

## 14.2.4 (2014-09-28)

### New

* add new munin plugin version and version update for base image. [Thomas Merkel]

### Changes

* update changelog file. [Thomas Merkel]

## 14.2.3 (2014-09-27)

### Other

* update changelog. [Thomas Merkel]
* yes we know what we are doing, so please install rsyslog. [Thomas Merkel]

## 14.2.2 (2014-09-23)

### Other

* update changelog. [Thomas Merkel]
* update changelog. [Thomas Merkel]
* update version. [Thomas Merkel]
* install rsyslog via customize script. [Thomas Merkel]
* use new version of rsyslog. [Thomas Merkel]

## 14.2.1 (2014-09-23)

### Other

* version update. [Thomas Merkel]
* version update. [Thomas Merkel]
* update license file. [Thomas Merkel]
* missing rsyslog gnutls. [Thomas Merkel]

## 14.2.0 (2014-09-21)

### Other

* add changelog. [Thomas Merkel]
* svcadm refresh is required to have new config enabled. [Thomas Merkel]
* fix readme. [Thomas Merkel]
* update readme file. [Thomas Merkel]
* Expired mozilla root ca's aren't my business so don't warn me for that. [Thomas Merkel]
* Disable StatelessAddrConf for all interfaces. [Thomas Merkel]

    We configure ipv6 manually and ndpd spams to the log file every minute
    with &quot;in.ndpd[2477]: [ID 102006 daemon.error] prefix_update_k(net1,
    net1:2, xxxx:xx:xxx:xxx::/64) from  to ONLINK AUTO  name is already
    allocated&quot;

* run postalias. [Thomas Merkel]
* fix subshell file cat. [Thomas Merkel]
* add munin plugin pkg_audit. [Thomas Merkel]
* update to new smartos munin configs. [Thomas Merkel]
* we will not check for ssl certificates in /etc anymore. [Thomas Merkel]
* don't graph ramdisk iops. [Sebastian Wiedenroth]
* be sure we skip the directory on extract. [Thomas Merkel]
* ups. [Thomas Merkel]
* move munin plugin configuration to customize. [Thomas Merkel]
* create cronjob for ssl-expire check. [Thomas Merkel]
* add script that check ssl expire. [Thomas Merkel]
* configre ssh host keys via mdata for reprovisioning. [Thomas Merkel]
* be sure you create an ssh dir. [Thomas Merkel]
* Add mdata support for ssh root_authorized_keys. [Thomas Merkel]
* add spiped-configure script. [Thomas Merkel]
* allow also mail send without authentication. [Thomas Merkel]
* enable postfix. [Thomas Merkel]
* configure postfix with smarthost, user authentication and root email. [Thomas Merkel]
* modify readme for mdata value for postfix. [Thomas Merkel]
* Add postfix minimal configuration. [Thomas Merkel]
* use skylime pkgsrc mirror. [Thomas Merkel]
* fix version information. [Thomas Merkel]
* support more than one dot. [Thomas Merkel]
* support munin hostnames. [Thomas Merkel]
* add mdata information to readme. [Thomas Merkel]
* Add remote logging server variables. [Thomas Merkel]
* add description. [Thomas Merkel]
* Add munin-node as default. [Thomas Merkel]
* add first idea of metadata extra information. [Thomas Merkel]
* add default pkgs. [Thomas Merkel]
* Add mdata setup scripts and zoneinit. [Thomas Merkel]
* add manifest for base image. [Thomas Merkel]
* first import basics for base mibe. [Thomas Merkel]
