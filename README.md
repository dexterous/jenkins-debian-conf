Quick and dirty Jenkins setup
=============================

For Debian variants (built and tested on Ubuntu 10.04 Lucid Lynx & 10.10 Maverick Meerkat)

Assumptions:
-----------
* running Jenkins as a standalone app
* jenkins runs on AJP1.3 only
* fronted by apache, under context /jenkins via `mod_jk`
* all software is installed as non-standard (as in, not from deb repos); hence under `/opt`

`java: /opt/java/<ver>`

`jenkins: /opt/jenkins/<ver>.war`

Notes:
-----
* `libapache2-mod-jk` does not create a `/etc/apache2/mods-available/jk.conf`
* all jenkins commands (except *start*) are `curl`s to respective HTTP APIs
* `etc/init.d/jenkins` can be configured for startup using `update-rc.d jenkins defaults`
