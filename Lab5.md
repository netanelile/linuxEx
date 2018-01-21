
lab5: logging -- Tasks:
-----------------------
* log in to your server using a text-only console.

* log in to same server using ssh session.

* find out which terminal names are used for both logins.

  


lab5: logging -- Anwers:
------------------------
* log in to your server using a text-only console.
	ctrl+alt F2
	Login: nati-deb
	Pass: (my nati Deb password)
* log in to same server using ssh session.
	Open terminal on a different machine (centos machine)
	At the Debian machine (as root): 
	1. Go to the sshd_config file and permit root login:
		vi /etc/ssh/sshd_config
		#change the line: 
		PermitRootLogin yes
		:qa
	2. Resart the ssh service:
		service ssh restart
	3. ifconfig #To know the machine IP (for assertion laiter)
	4. ssh (debian machine IP)
	5. At The Debian Maachine assert that the Centos is connected:
		service ssh status
		#The Centos IP will be display as connected.		
	At thecentos machine: 
* find out which terminal names are used for both logins.
	who
