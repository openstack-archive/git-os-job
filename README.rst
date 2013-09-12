git-os-job
==========

git plugin to show the OpenStack job log for a commit

What is git-os-job?
-------------------

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

Examples
--------

Look at the jobs related to the ``HEAD`` commit, usually in a
development branch that has been submitted to gerrit using git-review_
already.::

  $ git os-job

.. _git-review: https://pypi.python.org/pypi/git-review

Look at the jobs related to the previous commit, such as when a
development branch has a series of independent changes in it::

  $ git os-job HEAD^1

Look at the jobs related to a specific commit by tag, such as after
submitting a release tag::

  $ git os-job version.tag

Contributing and Reporting Bugs
-------------------------------

Please use the bug tracker on the github repository to report
problems. Patches for improvements are welcome, too.

https://github.com/dhellmann/git-os-job
