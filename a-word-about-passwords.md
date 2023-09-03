# A Word About Passwords


## Password Security Standards

Passwords remain a primary form of authentication to a system. The [NIST Digital Identity Guidelines](https://pages.nist.gov/800-63-3/sp800-63b.html) include requirements for password length and complexity.


## Practical Implementation

Different stakeholder groups each play a unique role in successfully enforcing password security requirements for an information system. Roles and responsibilities may include the following:


## Users’ Responsibilities include:

Rather than creating shorter passwords, which are easier to remember but less secure, use randomly generated passwords using a password manager, such as [1Password](https://1password.com/).

![](/images/1Password_Randomly_Generated_Password.png)

1Password will also warn you if any of your passwords have been exposed in known breaches, by marching the credentials you supply against the [haveibeenpwned database of breached passwords](https://haveibeenpwned.com/Passwords).



## Developers’ Responsibilities include:

It’s recommended that web applications should be designed to do the following, in order to secure users’ login credentials:

Only allow users to create passwords that are a minimum of 8 characters in length. 
Disallow users from creating passwords that have been included in known breaches.
One way they can do this is by using the [haveibeenpwned API](https://haveibeenpwned.com/API/v3).

![](/images/juice-shop-login.png)



## Penetration Testers’ Responsibilities include:

Use fuzzing techniques, injecting common or breached passwords, such as those from [SecLists](https://github.com/danielmiessler/SecLists), into a web application penetration tool, such as or [Burp Suite](https://portswigger.net/burp/documentation/desktop/tools/intruder) or  [Zedd Attack Proxy (ZAP)](https://www.zaproxy.org/docs/desktop/addons/fuzzer) 

![](/images/seclists-leaked-or-common-passwords.png)
