# h6 February2025!

## x) Read or watch and summarize

### 2.3 ONE-WAY FUNCTIONS

* One-way functions are easy to compute but hard to reverse.
* One-way functions can't be decrypted, therefore they're not useful as an encryption method.
* A trapdoor one-way function is a type of function with a, you guessed it, trapdoor.
    * Like the normal one-way function, they are easy to compute but hard to reverse, but if you know the secret you can easily reverse it.

### 2.4 ONE-WAY HASH FUNCTIONS

* A one-way hash function is a key part of modern cryptography.
* A hash function takes a input string (called a *pre-image*) and converts it into fixed lenght output string (called a *hash value*)
* A good one-way hash function is collision-free.
* A hash value is basically the fingerprint of a file. If you want to confirm you and someone else have the same file, you can compare the hash values.
   * If even a bit is changed in the original file, the hash value will be different.

## a) Install Hashcat

To install hashcat and the other necessary tools to crack hashes you need to run the commands:

    sudo apt-get update
    sudo apt-get -y install hashid hashcat wget

 After that let's create a directory to work in:

    mkdir hashed
    cd hashed
    
Now let's get to work wahoo. 
To properly crack a hash we need a dictionary. A dictionary (in this case) contains the most used leaked passwords.

We'll download rockyou.txt, the most popular dictionary out there:
    
    wget https://github.com/danielmiessler/SecLists/raw/master/Passwords/Leaked-Databases/rockyou.txt.tar.gz

Then we'll extract the dictionary and remove the archive file by running the following commands:

    tar xf rockyou.txt.tar.gz
    rm rockyou.txt.tar.gz

![hashcat-01](https://github.com/whatmurder/information-security/blob/main/img/h6-a-01.png)

Now we have all the tools we need to work with. For the actual hash we're gonna crack we're just using the `6b1628b016dff46e6fa35684be6acc96` provided to us.

First we have to identify the type of hash we have by running the command:

    hashid -m 6b1628b016dff46e6fa35684be6acc96

![hashcat-02](https://github.com/whatmurder/information-security/blob/main/img/h6-a-02.png)

After the command has run, we now have an analyzed hash. Now all that's left is to crack it.

We're gonna assume that the hash is a MD5 hash, since it's the most common one, and use that in the following command.

    hashcat -m 0 '6b1628b016dff46e6fa35684be6acc96' rockyou.txt -o solution

Here's a lil breakdown of what each part of the command does:

![hashcat-03](https://github.com/whatmurder/information-security/blob/main/img/h6-a-03.png)

Here's the actual cracking:

![hashcat-04](https://github.com/whatmurder/information-security/blob/main/img/h6-a-04.png)

Wow we cracked it. Now let's see the solution:

    cat solution

![hashcat-05](https://github.com/whatmurder/information-security/blob/main/img/h6-a-05.png)

Oh yeah.

## b) Crack this hash

Ok now let's try to crack this hash `d595b2086532422bbe654bc07ea030df` using what we learned in the previous exercise.

Let's scan the hash:

    hashid -m d595b2086532422bbe654bc07ea030df

![hash-crack-01](https://github.com/whatmurder/information-security/blob/main/img/h6-b-01.png)

We'll assume it's MD5 again. Let's try cracking it:

    hashcat -m 0 'd595b2086532422bbe654bc07ea030df' rockyou.txt -o answer

![hash-crack-02](https://github.com/whatmurder/information-security/blob/main/img/h6-b-02.png)

Now let's reveal the answer:

    cat answer

![hash-crack-02](https://github.com/whatmurder/information-security/blob/main/img/h6-b-03.png)

Cool beans we did it.

### Sources:

https://terokarvinen.com/information-security/

https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/10_chap02.html#chap02-sec003

https://terokarvinen.com/2022/cracking-passwords-with-hashcat/
