# Deploy_JBoss_App
Deploy JBoss EAP application
This is an Ansible Playbook containing a single role.  It uses the JBoss module to deploy a Java application
to an existing EAP environment

## Dependencies
An existing JBoss EAP environment

## Ansible Playbook
* site.yml - Single play which calls one role

## Extra Variables
Can be used to set the `java_app` variable which equates to the name of the `.war` file you wish to deploy.

## Roles
* java-app - This role copies and deploys a .war file to an EAP server using the copy and jboss modules

## Role Variables
* jboss_app - Define this variable as a .war file that exists in the `files` role directory.  By default, this is set to `ticket-monster.war`
but can be overridden by Extra Variables on the command line or Ansible Tower.
