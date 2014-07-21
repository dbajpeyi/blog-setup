# blog-setup

Magically bring up [blog-client](https://github.com/caulagi/blog-client)
and [blog-server](https://github.com/caulagi/blog-server).

* Install virtualenv, vagrant, virtualbox and ansible

```
$ sudo apt-get install python-virtualenv vagrant virtualbox
$ virtualenv ~/venv/blog
$ source ~/venv/blog/bin/activate
$ pip install ansible
```

* Set it rolling 

```
$ vagrant up ;# Ignore error about - failed to mount folders in Linux guest.
$ vagrant provision
```

### Troubleshoot -

**Q** The executable 'ansible-playbook' Vagrant is trying to run was not
found in the PATH variable.

**A**  You are not inside the virtualenv


**QED!**  Goto http://127.0.0.1:8002/blog.  Or login to the box with ```vagrant ssh```
