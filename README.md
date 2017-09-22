romaincabassot.sendmailrelay
=========

Version : 1.0.0

Install Sendmail and configure it to masquerade addresses and relay all messages to another SMTP server. 

Requirements
------------

[//]: # "Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required."

Role Variables
--------------

[//]: # "A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well."

- **sendmailrelay_masquerade_as**: the domain to masquerade addresses as 
- **sendmailrelay_smarthost**: the smtp relay host
- **sendmailrelay_smarthost_port**: the smtp relay port
- **sendmailrelay_queue_flush_freq**: frequency of sendmail's queue flushing 


Dependencies
------------

[//]: # "A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles."

Example Playbook
----------------

[//]: # "Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:"

    - hosts: servers
      roles:
         - {
             role: sendmailrelay, 
             sendmailrelay_masquerade_as: "mydomain.com",
             sendmailrelay_smarthost: "mysmtprelay.mydomain.com",
             sendmailrelay_smarthost_port: 25,
             sendmailrelay_queue_flush_freq: "1h"
           }
           
 

License
-------

BSD

Author Information
------------------

Romain CABASSOT
