nginx
======

Basic Nginx webserver


Role Variables
--------------

Mandatory vars : 

    - nginx_website_name : name of th ewebsite (generaly fqdn)
    - nginx_website_conf : configuration file (see samples)


See default/vars.yml for optionnal vars


Sample
------


- hosts: webservers
  vars:
    nginx_website_name: myserver.mydomain.tld
    nginx_website_conf: |
        server {
            server_name   myserver.mydomain.tld;

            location / {
                root   /www/mydomain;
            }
        }

  roles:
    - nginx

License
-------

Licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

Author Information
------------------
Benjamin Jolivot
bjolivot@gmail.com
See my other "work on my computer" ansible things on https://www.github.com/bjolivot
