# todo-setup

Magically bring up [todo-client](https://github.com/caulagi/todo-client)
and [todo-server](https://github.com/caulagi/todo-server).

* Install ansible.

```
$ mkvirtualenv todo
$ pip install ansible
```

* Install vagrant and virtualbox

```
$ sudo apt-get install vagrant virtualbox
```

* Set it rolling 

```
$ workon todo
# Ignore error about - failed to mount folders in Linux guest.
$ vagrant up
$ vagrant provision
```

### Troubleshoot -

**Q** The executable 'ansible-playbook' Vagrant is trying to run was not
found in the PATH variable.

**A**  You are not inside the virtualenv



**QED!**  Goto http://127.0.0.1:8002
