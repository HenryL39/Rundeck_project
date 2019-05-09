# Rundeck_project
Usage :
use playbook site.yml to execute all 3 playbooks for tomcat, apache and Rundeck

Details :
tomcat.yml creates a tomcat server

apache.yml creates an apache server which is acting as reverse proxy onto the rundeck server

rundeck.yml creates a rundeck server and configure it like so :
username : admin
password: admin

New node created pointed towards tomcat
New project names monitoring created using the tomcat node (called Tomcat2)
New job created in the project which clears all logs from the tomcat server every night a 0:00
