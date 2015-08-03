Role Name
=========

This role aims to install a working version of the ticketing software [Brimir](https://github.com/ivaldi/brimir) (with Apache2, PostgreSQL and sendmail).

Special thanks to frenkel, Brimir's maintainer !


Requirements
------------

No requirements.

Role Variables
--------------

**passenger_key** : This is the key for the passenger repo. The default is tuned for Debian 8 (Jessie). If you want another key, please visit [Passenger's documentation](https://www.phusionpassenger.com/documentation/Users%20guide%20Apache.html)


**install_path** : This is the path where Brimir will be installed. Default is /root/brimir, feel free to modify it according to your environment.


**user_email** : this is the first user (first user that will be created, allowing you to login) 's email address. 


**user_password** : Again, this is the first user's password. I would recommend you to create a dumb password, and then modify it from Brimir.


**sender_mail** : This is the email address Brimir will be using to send notifications.


**brimir_host** : This is Brimir's URL (example : support.domain.com).

**listen_address** : The address on which Passenger will listen. Default is 0.0.0.0

**listen_port** : The port on which Passenger will listen. Default is 3000
Example Playbook
----------------


    - hosts: brimir_server
      roles:
         - { role: thehunt33r.brimir, user_email: 'test@domain.com'       user_password: 'root' }

License
-------

BSD

Author Information
------------------

If you want to contact me, please do so at matthieu@matthieu-antoine.me
