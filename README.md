Role Name
========

Install [Atlassian jira](https://www.atlassian.com/software/jira)

Requirements
------------

A database, either PostgreSQL or MySQL, running somewhere.

Role Variables
--------------

All defined in defaults, so overrideable:

    jira:
      version:   5.4.4
      baseurl:   http://www.atlassian.com/software/jira/downloads/binary
      installer: atlassian-jira-5.4.4.tar.gz
      user:      jira
      # use postgresql or mysql
      dbconnector: postgresql
      packages:
        - java-1.7.0-openjdk
      tmp:       /var/tmp
      installto: /opt
      datadir:   /srv/jira-data


Dependencies
------------


Example Playbook
-------------------------

    - hosts: jira_servers
      roles:
         - { role: jira }

License
-------

MIT/BSD

Author Information
------------------

Mark Phillips <mark@probably.co.uk>
http://probably.co.uk
