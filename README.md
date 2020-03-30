# Email Checker

First you need to install java and install it

Second thing you need to run (open) java index.jar file 

### Install

```
npm install -g email-verify
```

#### Important Note

If you upgrade to > 0.0.12 from a previous version, you will need to make minor changes in your code. The callback was made to be error first.

### Usage
You can use it stand alone with the email-verify command and as many email addresses as you want to check.

```
email-verify addr1@domain.com addr2@anotherdomain.com
```

Using -d

```
email-verify -d domain.com addr1 addr2 addr3
```

Using -d -s, checking the standard email addresses

```
email-verify -d domain.com -s
```

Using -d -n, checking for variations of a name [-n firstname lastname]

```
email-verify -d domain.com -n firstname lastname
```

Using it in a more complicated way

```
email-verify -d domainA.com addr1 addr2 -n firstname1 lastname1 -d domainB -n firstname2 lastname2
```

Each time you use -d, it treats everything after it as that domain until another domain is used. Until you use -d, it treats it as there is no domain so you can't do -s or -n.
