Contributing to ZeroTier Role
=============================

Requirements
------------

Development and testing is currently using Python 3.7, Ansible 2.8 and Docker.

Create a Python virtualenv and run (this command will install dependencies from
both PyPI and Ansible-Galaxy)::

    make galaxy-requirements

Ensure you also have a local Docker environment available.

Testing
-------

To test the current version of Ansible installed in the virtualenv against all
of the supported Linux platforms, run::

    make test

To minimize the time taken to make changes and run tests, first run `make setup`
to create and initialize the Docker containers. Then run `make test-only` to
execute the test playbook against the containers, and repeat as needed until the
tests pass. Finally, run `make cleanup` to destroy the Docker containers.

Suggestions
-----------

*   If you're wanting to make larger changes or feature additions, consider
    opening an issue first for discussion.
*   Don't forget to update README.md if any role parameters are changed.

