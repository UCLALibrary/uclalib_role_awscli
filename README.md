uclalib_role_awscli [![Build Status](https://travis-ci.org/UCLALibrary/uclalib_role_awscli.svg?branch=master)](https://travis-ci.org/UCLALibrary/uclalib_role_awscli)
=========

This Ansible role installs the AWS command line tools.

Role Variables
--------------

There are three default variables for this role that can be overridden if needed:

    pip: python-pip
    pip_awspkg: awscli
    pip_bin: /usr/bin/pip

Dependencies
------------

In order to use `pip` on RHEL 6.x, it must be first installed from the EPEL repository.

Example Playbook
----------------

A simple example playbook that overrides a default variable:

    ---
    
    - hosts: all
    
    # Optionally, reference pip_bin in a different location
    - pip_bin: /usr/local/bin/pip
    
    roles:
      - { role: uclalib_role_awscli }

License
-------

BSD 3-Clause

Author Information
------------------

For more information about this role contact its author, [Anthony Vuong](https://github.com/avu0ng).
