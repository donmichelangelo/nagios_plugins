# check_vhost_sites
This Plugin can automatically check all the Vhosts on your webserver for error codes.
The root cause for those error codes may vary. Sometimes it's the PHP-FPM pool of a website
that just hung up (while PHP-FPM in general is still running) or a coding error in your website
or a configuration mistake in the config of your Vhost.

check_vhost_sites does support the Apache and NGINX webserver.
The Vhosts are being detected on Apache systems by executing `apachectl -t -D DUMP_VHOSTS`
and on NGINX systems by executing `nginx -T -q`. 

** Requirements
This Plugin requires curl and the Nagios package (nagios-plugins on CentOS/RHEL / nagios-plugins-common on DEB/UBUNTU). 
