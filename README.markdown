debian-rails-bootstrap
======================

(c) 2011 Jason Frame [jason@onehackoranother.com]

Set up an Apache/REE/Passenger/Rails/MySQL stack in a swift single move.

Use at your own risk, preferably only on fresh install. Tested with Debian 6.

Usage
-----

Run the following commands, substituting the `$` prefixed variables as necessary:

    apt-get update && apt-get -y install ruby rake curl && curl -O https://raw.github.com/jaz303/debian-rails-bootstrap/master/bootstrap && chmod +x bootstrap
    # now edit configuration section of `bootstrap`
    ./bootstrap
    
Notes
-----

SSH:

  * is locked down to the 'ssh' group
  * has root login disabled
  * has password-based login disabled
  
The non-privileged user is automatically added to the `ssh` group, __but remember to add your public key to the authorized\_keys file or you will be locked out__!

TODO
----

  * alternative web servers - nginx/lighttpd
  * configure logrotate
  * install/configure Postfix for outgoing email
