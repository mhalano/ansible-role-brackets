brackets
========

This role download and install Adobe Brackets IDE in the specified version. I wrote this role to be compatible with systems based on Debian (there's no  RPM package for now), but I just tested on Ubuntu. Please report bugs.

Requirements
------------

No special requirements except Ansible 2.1. Need to be this version because the package is downloaded by the apt module and this feature begun to be delivered on this release.

Role Variables
--------------

release: 1.7 - This variable define which release will be downloaded and installed. The default is 1.7, the latest versiona available in the moment. Don't expect much changes on the default value. I will trust you to select the most recent version manually.
repo: { true|false } - This variable define if the repository from webupd8 should be added to the system. The default is true.

Dependencies
------------

No dependencies.

Example Playbook
----------------

Here an a simple example of a playbook:

    - hosts: localhost
      roles:
         - { role: brackets, brackets_release: 1.6 }

License
-------

MIT

Author Information
------------------

My name is Marcos H. Alano. This is my third role published on Ansible Galaxy. I wrote a lots of roles and I will porting one by one. Is all roles related to desktop applications (may be a few will be for server applications in the future) because my plan is automatize the post-installation of my computer.

To Do
-----

* Find a better way to deal with libgcrypt11 dependency
* Create a variable called "source" to define if the package will be downloaded from Atom website ("web") or from repository ("repo")
* Support macOS
* Find a way to add support for RPM-based distros
* Do tests on Debian distribution
* Support GenericLinux using a generic non-package format
