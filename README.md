# policy-systemhealth
System Health checker for Postfix integrated using same mechanism as postgrey

## Background

This uses the Postfix STMP Access Policy Delegation mechanism
http://www.postfix.org/SMTPD_POLICY_README.html

See also http://www.postfix.org/access.5.html

## Usage:

policy-systemhealth /etc/postfix/systemhealth.yml

### check_nfs_mount

A NFS server going down can be simulated by blocking the host in iptables, eg:

   # block
   iptables -A INPUT -s <IP Address> -j DROP
   # check
   iptables -nL
   # unblock
   iptables -F

### sssd_health

This runs sssctl to determine the health of the AD connection for the machine.

AD server downtime can be simulated using above technique of blocking the host.

### user_exists


## Dependencies

On Debian install the following packages:

* libyaml-perl
* libgetopt-long-descriptive-perl
* libarray-utils-perl
* libcapture-tiny-perl 
* libfile-which-perl
