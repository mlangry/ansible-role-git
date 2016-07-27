ansible-role-git[![Build Status](https://travis-ci.org/mlangry/ansible-role-git.svg?branch=master)](https://travis-ci.org/mlangry/ansible-role-git)
=========

Ansible role for installing and configuring git

Requirements
------------

None

Role Variables
--------------

````yaml
git_config_file: ~/.gitconfig
git_config:
  color:
    branch: auto
    diff: auto
    interactive: auto
    status: auto
    ui: auto
  core:
    editor: nano
    excludesfile: "~/.gitignore"
  alias:
    clo: clone
    co: checkout
    st: status
    pur: pull --rebase
    ci: commit
    rc: rebase --continue
    lg: log -M --decorate --graph --oneline
    br: branch
    sth: stash

git_ignore:
    - ".*"
    - "!.gitignore"
    - "!.htaccess"
    - "*~"
    - "*.log"
````

Dependencies
------------

None

Example Playbook
----------------

````yaml
    - hosts: all
      roles:
        - { role: mlangry.git }
````

License
-------

MIT
