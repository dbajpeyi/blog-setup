# todo-setup
[![Build Status](https://travis-ci.org/caulagi/todo-client.png?branch=master)](https://travis-ci.org/caulagi/todo-client)

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
$ vagrant up
$ vagrant provision
```

**QED!**  Goto http://127.0.0.1/todo/
