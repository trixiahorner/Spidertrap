# Spidertrap

## Introduction
Trap web crawlers and spiders in an infinite set of dynamically generated webpages! The Spidertrap lab is designed to demonstrate how we can create a web of decoy pages that ensnare automated web crawlers and malicious actors. 

## Walkthrough
We will be using a script file containing a list of webpage names to serve, one per line. If no file is provided, random links will be generated.
<br>
<br>
### Step 1: get IP of your Linux system and then cd into the proper directory
![IP](https://github.com/trixiahorner/Spidertrap/blob/main/images/s1.png?raw=true)
<br>
<br>
### Step 2: run script
```
python3 spidertrap.py
```
![script](https://github.com/trixiahorner/Spidertrap/blob/main/images/s2.png?raw=true)
<br>
<br>
### Step 3: visit your web server : port 8000 
```
http://172.28.3.40:8000
```
You should see a page containing randomly generated links. If you click on a link it will take you to a page with more randomly generated links. This is essentially the spidertrap.
<br>
<br>
![web](https://github.com/trixiahorner/Spidertrap/blob/main/images/s3.png?raw=true)
<br>
![web2](https://github.com/trixiahorner/Spidertrap/blob/main/images/s4.png?raw=true)
<br>
<br>
### Step 4: 
