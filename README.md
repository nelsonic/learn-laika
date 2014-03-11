#hello-laika

### Very simple meteor app with tests written with [laika](http://arunoda.github.io/laika/)

##[Documentation](http://arunoda.github.io/laika/)

### Trouble-Shooting

#### Trying to start MongoDB?

Laika requires its own MongoDB 
```
 mongod --smallfiles --noprealloc --nojournal
```

If you get the following error message (when trying to start **mongod**)

```sh
-bash: mongod: command not found
```

(On Mac) install mongodb using brew:

```
brew install mongodb
```

Now if you try to run the `mongod` command you might get the following error:

```
ERROR: dbpath (/data/db/) does not exist.
Create this directory or give existing directory in --dbpath.
```

We are going to opt for creating a db path in our project 
and tell mongod about it when we start the server.

```
mkdir db
```
Then (from inside the project directory) start mongodb with this command:

```
mongod --smallfiles --noprealloc --nojournal --dbpath ./db
```
![Imgur](http://i.imgur.com/p24irjR.png)



Then you can run the **laika** command:

```
laika
```

If everything is setup correctly you should see:

![Imgur](http://i.imgur.com/jxb7py2.png)