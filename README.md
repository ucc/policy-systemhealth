# postgrey-systemhealth
System Health checker for Postfix integrated using same mechanism as postgrey

## Background

This uses the Postfix STMP Access Policy Delegation mechanism
http://www.postfix.org/SMTPD_POLICY_README.html

See also http://www.postfix.org/access.5.html

## Usage:

postgrey-systemhealth /etc/postfix/systemhealth.yml

## Dependencies

On Debian install the following packages:

* libyaml-perl
* libgetopt-long-descriptive-perl
* libarray-utils-perl
