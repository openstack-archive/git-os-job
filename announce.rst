==================
 git-os-job 1.1.0
==================

.. tags:: git release python openstack

What is git-os-job?
===================

The OpenStack_ project stores the logs for all of the test jobs
related to a commit on http://logs.openstack.org organized by the
commit hash. To review the logs after a job runs, most developers
start with the message jenkins leaves on gerrit, and click through to
the log files. Not all jenkins jobs are triggered by or related to a
gerrit review, though (e.g, release tags). 

.. _OpenStack: http://openstack.org/

git-os-job makes it easy to find those logs by finding the hash of the
commit and using it to build the right URL. It will then either print
the URL or open a web browser directly.

What's New?
===========

- add --reverse option to go from log URL to review URL
- improve python 3 support
- add -u alias for --url option

Installing
==========

Download from PyPI: https://pypi.python.org/pypi/git-os-job

or install with pip::

  $ pip install git-os-job

More Details
============

See the project page on github for more details:

https://github.com/dhellmann/git-os-job
