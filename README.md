# Spidertrap

## Introduction
Trap web crawlers and spiders in an infinite set of dynamically generated webpages! The Spidertrap lab is designed to demonstrate how we can create a web of decoy pages that ensnare automated web crawlers and malicious actors. 

## Walkthrough
The following lab is from Antisyphon Training's Active Defense and Cyber Deception course. We will be using a script file containing a list of webpage names to serve, one per line. If no file is provided, random links will be generated.
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
### Step 4: Now we will rerun Spidertrap, but this time we will use it with a file. Web crawlers are looking for specific directories, so let's make it look more like a legit directory.
*kill the last Spidertrap session*
```
python3 spidertrap.py directory-list-2.3-big.txt
```
![web2](https://github.com/trixiahorner/Spidertrap/blob/main/images/s5.png?raw=true)
![web2](https://github.com/trixiahorner/Spidertrap/blob/main/images/s6.png?raw=true)
![web2](https://github.com/trixiahorner/Spidertrap/blob/main/images/s7.png?raw=true)
<br>
<br>
### Step 5: Finally, we will run Spidertrap one last time, but this time we will use wget to mirror the website
- (-m): This option stands for "mirror". It tells wget to download the entire website in a way that creates a local copy of the site. It will download not just the specified file but also any files linked from it, and so on. This option also allows for infinite recursion, so it will follow links to any depths.
```
sudo wget -m http://127.0.0.1:8000
```
![web2](https://github.com/trixiahorner/Spidertrap/blob/main/images/s8.png?raw=true)
![web2](https://github.com/trixiahorner/Spidertrap/blob/main/images/s9.png?raw=true)
<br>
<br>
Wget is a script to download files from the web, but  spidertrap is a tool that when an attacker gets into that folder, it keeps him in there. It’s crawling the cyber deception webpage, so it keeps crawling random pages. 
<br>

## Conclusion
By generating a labyrinth of infinitely nested and randomly generated pages, a spidertrap can exhaust an attacker’s resources, disrupt their activities, and provide crucial insights into their tactics. The concept of a spidertrap offers an active approach to defending web resources.
