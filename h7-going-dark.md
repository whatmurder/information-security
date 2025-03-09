# h7 Going Dark

## x) Read and summarize

### 7 Things You Should Know About Tor

1. NSA has tried to crack Tors anonymity, but have been unsuccesful at it. Only way they've found out someones identity is because of browser bugs or user mistakes.
2. Tor isn't only used by criminals! Families can use it to protect their children, and journalists can use it to safely communicate.
3. Tor is open source, and doesn't have any backdoors. If you want to check for yourself, you can go look at the source code.
4. In the USA, nobody has been prosecuted for running a Tor Relay. A Tor Relay is basically a checkpoint your connection goes through to help anonymize your connection to the site you're trying to reach.
5. Tor is easy to use! Just download it!
6. Tor has been getting faster over the years. 🏃💨
7. Tor doesn't guarante your anonymity. You need to use it correctly and keep everything updated to keep your anonymity safe.

### Hiding Behind the Keyboard: The Tor Browser

* Tor browser is a modified version of the Firefox browser. The modifications hides the users IP-address.
* Tor is one of the easiest ways to remain anonymous on the internet.
* Tor's intention is to enable anonymous communication on the internet.
* Using Tor a person can access websites that have been blocked in the country they live in, allows whistleblowers to communicate while remaining anonymous and enables anonymous conversations.
* Tor was developed by the US goverment, but the Tor network isn't controlled by a single entity. It's basically a group effort by users to improve/develop it.
* Tor directs the users Internet traffic through relays while connecting to a website. In the entry point the users data gets encrypted, and each of the relays strips a little bit of the users encryption. None of the relays points know anything about the previous relay points except the previous relay point.
* *"[...]sending data over Tor is like an onion, where a layer of encryption is peeled off as it goes through the Tor nodes to its final destination."*
* Goverments are working on deanonymizing Tor, but in most cases a criminal in the darkweb is caught by the mistakes the user has made instead of the goverment breaking Tor.
* The biggest weakness of Tor is the user.


## a) Install TOR browser and access TOR network (.onion addresses).

To install tor you first navigate to the Tor Project website: https://www.torproject.org/download/

Since we're on linux we click the `Download for Linux` button.

You should now have it downloaded on your computer and it should be in the location you chose. In my case it's in the downloads folder.

Now we open the terminal and locate to the downloads folder:

    cd Downloads

We've arrived. The file we downloaded is an archive, which means we have to exctract it to gain access to its contents.
In the terminal we run this command:

    tar xf tor-browser-linux-x86_64-14.0.7.tar.xz

Fun fact: I typed out that entire file name manually by hand!

Now if you didn't get any errors you should have a new directory in your downloads directory.

![extracted](https://github.com/whatmurder/information-security/blob/main/img/h7-a-01.png)

Then we go into that directory:

    cd tor-browser

Then to launch the Tor browser you run the command:

    ./start-tor-browser.desktop

![tor-launch](https://github.com/whatmurder/information-security/blob/main/img/h7-a-02.png)

We launched it!

![Tor not connected](https://github.com/whatmurder/information-security/blob/main/img/h7-a-03.png)

We're not connected to any network immediately, so now we just click the `Connect` button.

![Tor connected](https://github.com/whatmurder/information-security/blob/main/img/h7-a-04.png)

We're connected, let's get to browsing!

## b) Browse TOR network

### Search engine

Ahmia is a search engine that can find .onion sites

![ahmia](https://github.com/whatmurder/information-security/blob/main/img/h7-b-01.png)

### Marketplace

BusKill is a website where you can purchase USB-killcords for your laptop. 

![buskill-01](https://github.com/whatmurder/information-security/blob/main/img/h7-b-03.png)

*"What's a killcord?"* you may ask. This USB-killcord is a device/thingmajig/contraption/whatever that plugs into your laptop, and when removed - you guessed it - kills the laptop by either shutting it down or just wiping the thing

The website describes it better:

*"BusKill can trigger your laptop to lock, shutdown, or self-destruct if it’s physically separated from you."*

![buskill-02](https://github.com/whatmurder/information-security/blob/main/img/h7-b-04.png)

### Forum(s)

You can got on reddit on the darkweb. There's no escaping redditors...

![le narwhal bacons at midnight](https://github.com/whatmurder/information-security/blob/main/img/h7-b-05.png)

There's also a reddit-esque forum called Dread, which discusses darkweb related topics.

![DREAD](https://github.com/whatmurder/information-security/blob/main/img/h7-b-06.png)

Personal favourite: The fentanyl thread.

### A site for a well known organization that has a physical street address in the real world

CIA. I don't have a quip for this one.

![CIA](https://github.com/whatmurder/information-security/blob/main/img/h7-b-07.png)


### Sources:

https://terokarvinen.com/information-security/

https://www.eff.org/deeplinks/2014/07/7-things-you-should-know-about-tor

https://learning.oreilly.com/library/view/hiding-behind-the/9780128033524/XHTML/B9780128033401000021/B9780128033401000021.xhtml#s0010

https://www.torproject.org/download/

https://en.wikipedia.org/wiki/List_of_Tor_onion_services

http://juhanurmihxlp77nkq76byazcldy2hlmovfu2epvl5ankdibsot4csyd.onion/

http://www.buskillvampfih2iucxhit3qp36i2zzql3u6pmkeafvlxs3tlmot5yad.onion/

https://www.reddittorjg6rue252oqsxryoxengawnmo46qy4kyii5wtqnwfj4ooad.onion/

http://dreadytofatroptsdj6io7l3xptbet6onoyno2yv7jicoxknyazubrad.onion/

http://ciadotgov4sjwlzihbbgxnqg3xiyrg7so2r2o3lt5wz5ypk4sxyjstad.onion/
