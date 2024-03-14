Problem: There is a problem, every time I run the playbook the service get restarted.

Every time when I execute a playbook it restart's service ==> only restart the service when => the configuration is changed 
We can use WHEN condition for that, but ansible use much more better way, ie Handlers 


- handler not executed until they are notified by notified module
