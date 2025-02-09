# h4 Johnny Tables

## x) Read and summarize

### OWASP A01:2021 - Broken Access Control

* Broken access control happens when an user has more priviledges than they're supposed to have, granting them the ability to perform actions they shouldn't be able to do, i.e. wiping data from a database.
* To avoid this you should go over your application and go over what a user/group can do, rate limit API access and just deny everything an user can do if the resource isn't public.

### OWASP A05:2021 - Security Misconfiguration

* Security misconfiguration may occur if, well as the name says the application isn't configured properly. These misconfigurations may be missing security updates/updates in general, default accounts left on the software with default passwords, error messages with too much information for malicious actors to use or if there's just some unnecessary features are enabled.
* If you keep your system/application as lean and up-to-date as possible (security wise atleast) you're left in a much safer position.

### OWASP A06:2021 - Vulnerable and Outdated Components

* Sort of similiar to the previous one, Vulnerable and Outdated Components are exactly what the title says they are. Your software might have some dependencies and components you used in a previous version of it still remaining on it that you haven't removed or updated, or you've downloaded a fork of a component that isn't maintened anymore/is not as securely programmed as the official one, providing a malicious actor to take advantage of them.
* Preventing them is as easy as keeping up with what dependencies are installed/used in your application, updating and/or removing them as necessary. Also try to download your components from reputable, official sources. **Use common sense!!!**

### OWASP A03:2021 - Injection

* Injection is when the malicious actor inject custom code or something else that's nefarious that can lead to malicious code to be executed in the application. Injection can happen if user input isn't properly validated, or if the malicious actors can manipulate input fields, cookies, HTTP headers, or other data sources.
* Proper validation of user inputs can prevent injections.

### xkcd 327: Exploits of a Mom

* A comic where the puncline is that Bobby Tables is named in a way that when his name is typed into the school database, it wipes every student record
* There's a *XKCD* for everything

## a) Goat

Installing *Webgoat* was pretty straight forward by following the guide given, only thing that took a little more research was installing *wget*.
I thought I remembered how to install new programs on Linux but it seems I mistyped the install command, so I googled how to install it.

This is how I tried to do it at first:

    sudo apt get wget
    
Which of course didn't work. So I did a little googling and found out the proper command:

    sudo apt install wget

That worked and now we have wget on our Debian installation, wahoo.

After that I followed to guide again, launched *Webgoat*, made an account (after disconnecting from the internet of course) and tadah:

![Screenshot of Webgoat running](https://github.com/whatmurder/information-security/blob/main/img/h4-a-webgoat-installed.png)

## b) F12

## c) Not outdated

So I actually just installed this Debian instance today and fully updated it, but here's a screenshot of me updating and -grading it again:

![nothing to update](https://github.com/whatmurder/information-security/blob/main/img/h4-c-not-outdated.png)



## d) Sequel

## e)  Solve Portswigger Labs

### Sources:

https://terokarvinen.com/information-security/

https://owasp.org/Top10/A01_2021-Broken_Access_Control/

https://owasp.org/Top10/A05_2021-Security_Misconfiguration/

https://owasp.org/Top10/A06_2021-Vulnerable_and_Outdated_Components/

https://owasp.org/Top10/A03_2021-Injection/

https://xkcd.com/327/

https://terokarvinen.com/2023/webgoat-2023-4-ethical-web-hacking/

https://www.cyberciti.biz/faq/how-to-install-wget-togetrid-of-error-bash-wget-command-not-found/

https://sqlzoo.net/wiki/SQL_Tutorial

https://portswigger.net/web-security/sql-injection/lab-retrieve-hidden-data
