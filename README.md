Role Name
=========

A brief description of the role goes here.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------
All this files/Variables are REQUIRED and cannot be omitted.

domain_crt: inside vars/domaincrt.yml value is the domain.crt of the registry as ansible-vault
domain_key: inside vars/domainkey.yml value is the domain.key of the registry as ansible-vault
htpasswd_content: inside vars/htpasswd.yml value is the output of registry:2 htpasswd command to generate the BasicAuthentication value for your registry user. a pair of username:base64(password).

Dependencies
------------
ansible_docker_role: https://github.com/shelleg/ansible-docker-role.git
A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

- hosts: registry
  roles:
    - docker_host 
    - docker_registry
    

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
