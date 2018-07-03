Packages
========

Installs a default set of packages

Requirements
------------

None

Role Variables
--------------

    base_packages:
      - unzip
      - curl
      - htop
      - atop
      - vim
      - git
      - wget
      - libxml2-utils
      - screen
      - mount
      - tree
      - libpam-umask

A list of packages which will be installed

    additional_packages: []
    
Additional packages that will be installed without replacing the base_packages

    install_sendmail: false
    
Should sendmail be installed or not

    install_exim: false
    
Should exim be installed or not

    sendmail_packages:
      - sendmail
      
Packages that should be installed if `install_sendmail` is true

    exim_packages:
      - exim4-base
      - exim4-config
      - exim4-daemon-light
      
Packages that should be installed if `install_exim` is true

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: solutiondrive.packages }

Maintainer
----------

solutionDrive DevOps <developer@solutiondrive.de>
