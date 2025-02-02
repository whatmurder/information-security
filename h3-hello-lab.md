# h3 Hello Lab

*Notes: I wasn't able to make it class last time, so if there were some tips and tricks on what tools to use in the homework or if I'm doing something differently that's probably the reason.*

## x) Read/watch/listen

I've installed Debian and other Linux distros before so reading the documents weren't *that* necessary for me, but I still skimmed through them

![screenshot of my debian desktop and a terminal window where the neofetch command is used](https://github.com/whatmurder/information-security/blob/main/img/h3-deb-01.png)

I installed neofetch for fun because it's cool and I don't care that it's deprecated.

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

The two open ports were Port 80 for HTTP and Port 631 for IPP
