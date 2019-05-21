=======================================
Security notes for OpenStack components
=======================================

Installation
============
``virtualenv -p python3 .venv && source .venv/bin/activate``
``pip3 install git+https://github.com/vladiskuz/secnotes``


How to use
==========
secnotes --help
usage: secnotes [-h] [--gerrit GERRIT] [--workdir WORKDIR]
                [--gerrit-username GERRIT_USERNAME]
                [--gerrit-password GERRIT_PASSWORD] [--project PROJECT]
                [--start-commit START_COMMIT] [--end-commit END_COMMIT]

Analyze the git log from the start commit sha to the end commit sha, extract
references to bugs and then scan the bug tracker for security issues.

optional arguments:
  -h, --help            show this help message and exit
  --gerrit GERRIT       Gerrit url (full HTTP(S) URL).
  --workdir WORKDIR     The directory in which the project will be stored.
  --gerrit-username GERRIT_USERNAME
                        Gerrit HTTP user name to access Gerrit HTTP API/repos.
  --gerrit-password GERRIT_PASSWORD
                        Gerrit HTTP password.
  --project PROJECT     Gerrit project name.
  --start-commit START_COMMIT
                        Start commit SHA which must be before --end-commit in
                        the log history.
  --end-commit END_COMMIT
                        End commit SHA which must be after --start-commit in
                        the log history.
