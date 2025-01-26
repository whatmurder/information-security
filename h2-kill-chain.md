# h2 Kill Chain

## x) Read and summarize

### Intelligence-Driven Computer Network Defense Informed by Analysis of Adversary Campaigns and Intrusion Kill Chains in a nutshell

* The abstract and the introduction chapters introduce us to APTs (Advanced Persistent Threat)
	* APTs are well researched and (as their name suggests) advanced attacks that target highly sensitive economic, proprietary, or
national security information.
	* Unlike more common virus/malware attacks, APTs are manually operated calculated attacks that have extensive planning behind them. Anti-virus programs and vulnerability patching are not sufficient to prevent these types of attacks.
	* APT attacks usually follow a so called "Kill Chain", which consists of steps that the attack follows.

* Kill Chain is a systematic process to attack the desired target. The kill chain described in the paper consists of seven steps:
	1. Reconnaissance
 	2. Weaponization
  	3. Delivery
  	4. Exploitation
  	5. Installation
  	6. Command and Control
  	7. Actions on Objectives

 * By analyzing the kill chain the defender can develop a more robust defences against APTs and other types of attacks and can help the defender to slow down, stop or deter the possible attack.
	* The killchain model *"[...]serves as a framework to measure the effectiveness of the defenders’ actions"*

## a) Tactics, tools and procedures

### MITRE ATT&CK

1. Tactic
	* The reason for the attack
	* **Example:** The attacker wants to steal your Habbo Hotel account for themselves.

2. Technique: 
	* The method of the attack
 	* **Example:** The attacker is going to steal your password to gain access to your precious Habbo Hotel account with the rare vinyl player prop by *Phishing (T1566)*

3. Subtechnique
	* A more indepth look at the method of the attack.
 	* **Example:** The attacker sends you an email posing as the administrative staff of Habbo Hotel where you're prompted to change your credentials for security reasons with a link to fradulent password reset site. This is known as a *Spearphishing Link (T1566.002)*

4. Procedure
	* The exact steps the attacker takes in the attack.
	* **Example:** Attacker meticulously crafts the fake login page to trick you => They come up with an scenario as to why they have to send you a password reset email => They write out the email and send it to you => You, the poor victim, open the email and go into the fradulent password reset page and type out all of your information => The attacker now has your information and they proceed to log in to your account and change all the information so you can't get into it anymore. Now the attacker has all of your cool props and invites all of his friends to your room and hosts the most epic *Tuolari* ever and after that sells all your stuff for some extra *Kole*'s. 

### Sources

https://terokarvinen.com/information-security/#h2-kill-chain

https://lockheedmartin.com/content/dam/lockheed-martin/rms/documents/cyber/LM-White-Paper-Intel-Driven-Defense.pdf

https://www.lockheedmartin.com/en-us/capabilities/cyber/cyber-kill-chain.html

https://attack.mitre.org/

https://attack.mitre.org/resources/faq/#general-faq

