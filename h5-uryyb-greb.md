# h5 Uryyb, Greb!

## x) Read and summarize

fadasfasf

## a) Install OpenSSH server

sdgsddfgfgsg

## b) Automate SSH connection using public keys.

dasdsafsdgsdfgaf

## c) Pretty Good indeed

sdvsdgdhdfgsdgsdfg

## d) Password manager, open and cloudless

### Password manager pros

You should use secure passwords on all of your accounts, and coming up with secure ones that you can also remember is difficult. People tend to get lazy and would rather use a password they remember everywhere rather han come up with a new password. Here's where password managers come in to the picture: You'll only have to remember a single password!

Passwords managers (the good ones atleast) create a password protected database where the passwords are stored, and you can access it by using the master password. The manager can create a secure password for you, and it'll remember it for you also. Most password managers come with an option to autofill your account information so you don't even have to type it for yourself.

Using a password manager also helps you defend against multiple cyber attacks, i.e. brute force attacks and dictionary attacks.   

I personally use Bitwarden as my password manager of choice, it's open-source and free. I have it running on my browser as a browser extension and on my phone. I've used it for 4+ years by now.


For the sake of the exercise we'll use something locally running, and the manager I chose is KeePassXC. It's free, open-source and local. Wowzers.

### Installation

To install KeePassXC on Debian you run the command

    sudo apt install keepassxc

After the command runs its course, you can launch your freshly installed password manager from the applications menu.

![Installing KeePassXC, Part 01](https://github.com/whatmurder/information-security/blob/main/img/h5-d-install-keepassxc.png)

### Creating the password database

To create the password database you click the *Create new database* button.

![Installing KeePassXC, Part 02](https://github.com/whatmurder/information-security/blob/main/img/h5-d-keepassxc-create-database-01.png)

Then you enter a name for the Database.

![Installing KeePassXC, Part 03](https://github.com/whatmurder/information-security/blob/main/img/h5-d-keepassxc-create-database-02.png)

After that you can choose how to encrypt your database. I just left everything on the default settings.

![Installing KeePassXC, Part 04](https://github.com/whatmurder/information-security/blob/main/img/h5-d-keepassxc-create-database-03.png)

Then you create the only password you'll have to remember from now on, the password to unlock your vault. Make sure it's something you remember, and that it's as secure as possible.

![Installing KeePassXC, Part 05](https://github.com/whatmurder/information-security/blob/main/img/h5-d-keepassxc-create-database-04.png)

Then you choose the location to store the databse. I Created a folder that I'll delete after this exercise called *temp-pw-directory* and saved it there. 

![Installing KeePassXC, Part 06](https://github.com/whatmurder/information-security/blob/main/img/h5-d-keepassxc-create-database-05.png)

And now you have your password database up and running. To ass new passwords you press the + icon on the top left.

![Installing KeePassXC, Part 07](https://github.com/whatmurder/information-security/blob/main/img/h5-d-keepassxc-create-database-06.png)

Here's a screenshot of the adding a new password screen. You fill out the required info and you're set. For the password, you just click the 🎲 button in the password field.

![Installing KeePassXC, BONUS](https://github.com/whatmurder/information-security/blob/main/img/h5-d-keepassxc-create-database-07.png)

You can also install a browser extension to your browser of choise which I found interesting. I'll have to look into possibly moving my passwords to a local instance.

### Sources:

https://terokarvinen.com/information-security/

https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/08_chap01.html#chap01-sec006

https://terokarvinen.com/2023/pgp-encrypt-sign-verify/

https://keepassxc.org/download/#linux
