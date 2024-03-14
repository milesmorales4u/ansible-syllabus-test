

This exercise used to make NTP configureation file changes

Using 
	copy module
	file module
	template module



Update Ntp chrony file with our own file in ubuntu and alma linux
	1. create a template directory
	2. inside, create 2 template file
		one for alma and other for ubuntu
	3. copy the template content and update to template directory
		cat /etc/chrony.conf  ==> template/ntpconf_alma
		cat /etc/ntp.conf  ==> template/ntpconf_ubuntu
	4. update the playbook with template module (provisioning.yaml)


update the template add some data
	1.serch  for ntp server details
	2. inside grouup_vars/all
		add some variable of ntp servers
			eg: ntp0: server 0.in.pool.ntp.org
	3. update the variable inside template/ntpconf_alma and ubuntu
		eg: pool "{{ntp0}}" iburst

	4. run the playbook



Problem: There is a problem, every time I run the playbook the service get restarted.
