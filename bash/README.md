JavaScript
========================
## Sudo
If you forgot to put sudo and wanna have sudo on previous command you can use following command:
~~~bash
sudo !!
~~~

## CUT PASTE !
If you wanna cut the letters that are on the right side of your cursor you can use this command: ```ctrl+K```

And for the left side: ```ctrl+U```

And you can paste the removed text with ```ctrl+Y```.

And to cut previous word you can use : ```ctrl+W```.


## Git store
With the following command you can store credential of git:
~~~shell
git config credential.helper store
~~~

## Save SSH ID
~~~shell
ssh-copy-id username@server_ip -p <port>
~~~

## Background Tasks
To run your process or command/shell script in the background, include an & (an ampersand) at the end of the command/shell script you use to run the job. For example:
~~~shell
command &
~~~
One can bring a background process to the foreground such as sleep command using the fg command:
~~~shell
fg %n
fg %2
~~~

Kill a running process named “sleep 10000” using the kill command:
~~~shell
kill %n
kill %2
~~~
