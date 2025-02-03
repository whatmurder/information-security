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

## d) Bandit oh-five

### Level 0

I'm not familiar at all with SSH, so this level took a bit of internet browsing and research to figure out how to do.

Eventually I got the correct answer by logging in to the game by running this comman in the terminal:

    ssh bandit0@bandit.labs.overthewire.org -p 2220

![level0](https://github.com/whatmurder/information-security/blob/main/img/h3-deb-07.png)

The *-p* specifies which port to connect to.

### Level 1

Level one was easy, all it took was the commands *ls* and *cat*

![level1](https://github.com/whatmurder/information-security/blob/main/img/h3-deb-08.png)

Doing that I got the password for the next level. Yippee!

### Level 2

I logged out of the bandit0 user by just typing *exit* to the terminal, and then I logged into the bandit1 account using the command

    ssh bandit1@bandit.labs.overthewire.org -p 2220

and typing the password I got from the previous level.

After that I navigated to the bandit1 directory and found the file *-*

![level2-a](https://github.com/whatmurder/information-security/blob/main/img/h3-deb-09.png)

I tried doing the same thing as I did in the previous level, but the command didn't work and got stuck and I had to forcefully stop it using *ctrl+c*

I did a little Googling and found a stackoverflow article that helped me solve this problem. By just typing *cat -* the command line thinks you're going to type an arguement to the command, so typing *cat ./-* bypasses this and specifies that it's a file and it's found from the location that it's in.

![level2-b](https://github.com/whatmurder/information-security/blob/main/img/h3-deb-10.png)

Wow! Onto the next level.

### Level 3

Log out of bandit1, then log into bandit2. After logging in I ran the *ls* command and found that there's a file called *spaces in this filename*. Because I'm lazy and didn't want to type the full filename I did this:

    $ cat sp

Then I pressed the Tab key which autocompletes the command/directory/file/etc. what you're typing. and now my terminal line looked like this:

    $ cat spaces\ in\ this\ filename

I pressed enter and we got the password!

![level3](https://github.com/whatmurder/information-security/blob/main/img/h3-deb-11.png)

Level 4 time...

### Level 4

Log out => log in, the same thing as in every previous step so far. I ran the *ls* like before and founda directory called *inhere*. I went to the directory and ran *ls* again and found nothing! How could this be!!!!! 

Anyways I ran *ls -a* which shows every item, be it a file or a directory, even the hidden ones in the directory you're in. 

I found the file *...Hiding-From-You* and then I just showed it's contents using cat:

![level4](https://github.com/whatmurder/information-security/blob/main/img/h3-deb-12.png)

Hooray, all done! 

These were pretty fun and I might do the rest of them in the future if I'm bored.

### Sources:

https://stackoverflow.com/questions/42187323/how-to-open-a-dashed-filename-using-terminal

