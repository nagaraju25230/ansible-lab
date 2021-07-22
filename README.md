## Lab

* Create a playbook to install Apache2
* Apache2 should have customized configuration as well, the sample config is attached herewith
* You should provide the port number in the form of variable. eg. ```port_no``` is a variable name over here
* Change the port from 80 to 81 in the apache2.conf file, and take it to your client machine at the location ```/etc/apache2/sites-enabled/000-default.conf```
* Change the port from 80 to 81 in the port.conf file, and take it to your client machine at the location ```/etc/apache2/ports.conf```
* Restart of Apache2 is mandaotry when any config file is getting updated, so use Handler for that
* The default of apahce2 should have content like ```Hello, The hostname of this machine is ....... and the IP is .......```


