# todo-setup

Coming soon... a [Vagrant](http://www.vagrantup.com/) project
that will automate setting up [todo-client](https://github.com/caulagi/todo-client)
and [todo-server](https://github.com/caulagi/todo-server)

For now, you have to complete the steps manually -

### Setup [todo-server](https://github.com/caulagi/todo-server)

```
$ mkvirtualenv todo
$ pip install -r requirements.txt
$ python runserver.py
```

### Setup [todo-client](https://github.com/caulagi/todo-client)

```
$ sudo npm install -g grunt-cli
$ grunt build
```

### Setup nginx

```
$ cd /etc/nginx/conf.d
$ sudo ln -s /home/pcaulagi/jipu/src/todo-setup/todo.conf
$ sudo nginx -t
$ sudo nginx -s reload
```

**QED!**  Goto http://127.0.0.1/todo/
