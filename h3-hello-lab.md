# h3 Hello Lab

*Notes: I wasn't able to make it class last time, so if there were some tips and tricks on what tools to use in the homework or if I'm doing something differently that's probably the reason.*

## x) Read/watch/listen

I've installed Debian and other Linux distros before so reading the documents weren't *that* necessary for me, but I still skimmed through them

![screenshot of my debian desktop and a terminal window where the neofetch command is used](https://github.com/whatmurder/information-security/blob/main/img/h3-deb-01.png)

I installed neofetch for fun because it's cool and I don't care that it's deprecated.

here's the command to install neofetch:

    sudo apt install neofetch

Some thoughts on the reading material and the Debian installation:

* The *Command Line Basics Revisited* document is in my opinion super useful and should probably be taught to everybody who comes to study computer science in Haaga-Helia 
* I haven't used the *XFCE* desktop enviroment before, it seems fairly lightweight and easy to use for beginners. Visually I don't enjoy it that much, I prefer *Gnome* over it.

## a) Can't fish

So as I said earlier I wasn't in class so the method I used for this exercise was just to disconnect myself from the internet. 

### Ping Command:
![Ping command](https://github.com/whatmurder/information-security/blob/main/img/h3-deb-02.png)

I let it ping three times

### Ping command that doesn't go through:
![Ping that doesn't ping](https://github.com/whatmurder/information-security/blob/main/img/h3-deb-03.png)

I just disabled the internet connection. It did the trick. I technically passed.

## b) Local only

In this exercise I installed the tools that the Hints section told me to install

    sudo apt install nmap -y

The I disabled my internet connection again and ran the command:

![Terminal after running nmap](https://github.com/whatmurder/information-security/blob/main/img/h3-deb-04.png)

The two open ports were Port 80 for HTTP and Port 631 for IPP.

## c) Daemon 😈

I installed both apache2 and ssh following the instructions in the Hints section, and out of the two I decided to use the ssh

So at first I ran the command (program? Idk if it's a program or not. Maybe a process?) like this:

    sudo systemtcl start ssh

And after that to show that it was running I ran this command:

    sudo systemtcl status ssh

![sudo systemtcl status ssh](https://github.com/whatmurder/information-security/blob/main/img/h3-deb-05.png)

Wow it works and runs like a dream 🐎

Then to the actual exercise. I ran the same nmap command from the previous exercise and here's what that looked like:

![nmap with the daemon ooh wow](https://github.com/whatmurder/information-security/blob/main/img/h3-deb-06.png)

The difference between the previous nmap and this one is that we have an additional port open, the port 22, which is used by the OpenSSH. Cool!

