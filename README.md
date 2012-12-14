OpenLDAP schemas for OpenAM

Overview
 
* cn={98}netscape.ldif
  converted 02common.ldif in 389-ds-base-1.2.10.14
  http://repos.fedorapeople.org/repos/rmeggins/389-ds-base/epel-6/SRPMS/389-ds-base-1.2.10.14-1.el6.src.rpm

* cn={99}openam.ldif
 converted 99-user.ldif in openam

Usage:
  copy schemas to /etc/openldap/slapd.d/cn=config/cn=schema
 
Author: 
 Hiroyuki Sato.

Contact: 
  hiroysato at gmail.com

Problem:
 Currently only role and filter role work.
 (User and group does not work correctly.)
