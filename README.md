cpanel-logrotate
============================

#Adding hook

To add the hook into cPanel, you should use the code below:

``` bash
/usr/local/cpanel/bin/manage_hooks \
add script /opt/makerotate/makefile \
--stage post \
--category Stats \
--event RunAll
```
	
It will add a hook to the `Stats` category, so when stats is updated, nginx will do a reload.
