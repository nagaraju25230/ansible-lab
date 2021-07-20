## Lab
* Create a playbook to install Apache2
* Apache2 should have customized configuration as well, the sample config is attached herewith
* Change the port from 80 to 81 in the apache.conf file, and take it to your client machine at the location ```/etc/apache2/sites-enabled/000-default.conf```
* Change the port from 80 to 81 in the port.conf file, and take it to your client machine at the location ```/etc/apache2/ports.conf```
* Make sure you restart apache2 after updating config
* The default of apahce2 should have content like ```Hello, The hostname of this machine is ....... and the IP is .......```

Soultion-
```
---
- hosts: lab
  tasks:
    - name: install apache
      apt:
        name: apache2
        state: present
    - name: update config
      copy:
        src: apache.conf
        dest: /etc/apache2/sites-enabled/000-default.conf
    - name: update port config
      copy:
        src: port.conf
        dest: /etc/apache2/ports.conf
    - name: service restart
      service:
        name: apache2
        state: restarted
    - name: update html file
      template:
        src: demo.html
        dest: /var/www/html/index.html
```
