.. _ddc_install:

============
Installation
============

Tools are distributed as a package for selected operating systems. The package must be installed on your frontend alongside with the server packages. Additional Ruby dependencies and Ansible need to be installed manually as well. All these 3 installation steps must be done.

The requirements:

* **OpenNebula** 5.6.1 and above
* **Ansible** 2.5.x

Supported platforms:

* CentOS/RHEL 7
* Ubuntu 14.04, 16.04, 18.04
* Debian 9

1. Tools
========

Installation of tools is as easy as install of the operating system package. Choose from the sections below based on your operating system. You also need to have installed the OpenNebula :ref:`front-end packages <frontend_installation>`.

CentOS/RHEL 7
-------------

.. prompt:: bash $ auto

   $ rpm -ivh opennebula-provision-5.6.0-1.noarch.rpm

Debian/Ubuntu
-------------

.. prompt:: bash $ auto

   $ dpkg -i opennebula-provision_5.6.0-1_all.deb

2. Ruby dependencies
====================

When the package is installed, the Ruby dependencies need to be installed via the ``install_gems`` script.

.. prompt:: bash $ auto

   $ /usr/share/one/oneprovision/install_gems

3. Ansible
==========

It's necessary to have ``Ansible`` installed. You can use a distribution package if there is suitable version. Otherwise, you can install the required version via ``pip``:

.. prompt:: bash $ auto

   $ pip install 'ansible>=2.5.0,<2.6.0'

Check the ``Ansible`` is installed properly:

.. prompt:: bash $ auto

   $ ansible --version
   ansible 2.5.3
     config file = /etc/ansible/ansible.cfg
     configured module search path = [u'/root/.ansible/plugins/modules', u'/usr/share/ansible/plugins/modules']
     ansible python module location = /usr/lib/python2.7/site-packages/ansible
     executable location = /usr/bin/ansible
     python version = 2.7.5 (default, Apr 11 2018, 07:36:10) [GCC 4.8.5 20150623 (Red Hat 4.8.5-28)]
