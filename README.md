OpenLDAP schemas for OpenAM
===========================

Overview
--------
 
* cn={99}openam.ldif
 converted 99-user.ldif in openam

Usage
------
### Copy schema file 

* Copy schema file(cn={99}openam.ldif) into /etc/openldap/slapd.d/cn=config/cn=schema

### Modify cn={1}core.ldif 

#### Before

    olcObjectClasses: {15}( 2.5.6.17 NAME 'groupOfUniqueNames' DESC 'RFC2256: a gr
    oup of unique names (DN and Unique Identifier)' SUP top STRUCTURAL MUST ( uni
    queMember $ cn ) MAY ( businessCategory $ seeAlso $ owner $ ou $ o $ descript
    ion ) )

#### After

move uniqueMember entry into MAY element.

    olcObjectClasses: {15}( 2.5.6.17 NAME 'groupOfUniqueNames' DESC 'RFC2256: a gr
    oup of unique names (DN and Unique Identifier)' SUP top STRUCTURAL MUST (
    cn ) MAY ( uniqueMember $ businessCategory $ seeAlso $ owner $ ou $ o $ descript
    ion ) )

 
Author 
------
Hiroyuki Sato.

Contact 
-------

  hiroysato at gmail.com
