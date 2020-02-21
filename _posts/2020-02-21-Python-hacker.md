---
layout: article
title: "All You Need to Know about Ethical Hacking using Python"
date: 2020-02-21 11:09:00+0200
coverPhoto: https://i.udemycdn.com/course/750x422/2310306_6ffa_2.jpg
---

It is common practice amongst ethical hackers to write nifty scripts and automate any structured process, ranging from small network scans to wide area network packet sniffing. In recent years, Python has become the language of choice for such tasks, and there are good reasons for this. In this article on ethical hacking using Python, we will discuss the reasons that make these two such a brilliant couple

#Below is the list of topics we shall be going over:

* What is ethical hacking?
* What is Python?
* Why use Python for ethical hacking?
* Simple dictionary attack using Python

# What is Ethical Hacking?
The term hacking goes a long way back. To be exact, it all started at the Railroad Club of MIT, where both the term ‘hacking’ and ‘hacker’ were first coined. It’s been almost 50 years now, and hacking has evolved into a discipline in the current day and age. With the increase in awareness regarding data protection and data privacy, hacking has been deemed as an illegal activity today. If caught, there’s a good chance that you will be prosecuted for quite some time depending on the degree of harm caused.

None the less, to protect themselves from hackers of all sorts, employment of Ethical Hackers has become a common practice amongst organizations. Ethical hackers are given the responsibility of finding and fixing security flaws for a certain organization before black hat hackers find them.

# What is Python?
Python cheat sheet for beginner-EdurekaPython is a general-purpose scripting language that has gained immense popularity amongst professionals and beginners for its simplicity and powerful libraries. Python is insanely versatile and can be used for almost any kind of programming. From building small scale scripts that are meant to do banal tasks, to large scale system applications – Python can be used anywhere and everywhere. In fact, NASA actually uses Python for programming their equipment and space machinery. 

Python can also be used to process text, display numbers or images, solve scientific equations, and save data. In short, Python is used behind the scenes to process a lot of elements you might need or encounter on your devices.

# Why use Python for Ethical Hacking?
Python has gained its popularity mostly because of its super powerful yet easy to use libraries. Sure Python has awesome readability and it is really simple and all but nothing really beats the fact your job as a developer is made super simple with these libraries. These libraries find uses in all sorts of domains, for example, artificial intelligence has Pytorch and Tensorflow while Data Science has Pandas, Numpy, Matplotlib.

# Cyber Security Training
Similarly, Python is brilliant for ethical hacking for the following reasons:

Nifty python libraries like Pulsar, NAPALM, NetworkX etc make developing network tools a breeze
Ethical hackers generally develop small scripts and python being a scripting language provides amazing performance for small programs
Python has a huge community, hence any doubt related programming is quickly solved by the community
Learning Python also opens up your doors to several other career opportunities
Demo: Dictionary Attack using Python
Let me give you guys a small demonstration as to how an ethical hacker may use Python in his day to day job. Suppose you were scanning for a 3-way handshake between an FTP server and a client and you were successful in doing so too. But as you guys might already know, passwords are never really stored in plain text. They are always hashed before being stored in a database and normally the hash itself is compared for verification purposes. Let us create a small Python program that can be used to crack a password using the dictionary attack method.

```
	import hashlib
	 
	flag = 0
	 
	pass_hash = input("md5 hash: ")
	 
	wordlist = input("File name: ")
	try:
	    pass_file = open(wordlist,"r")
	except:
	    print("No file found :(")
	    quit()
	 
	for word in pass_file:
	 
	    enc_wrd =word.encode('utf-8')
	    digest =hashlib.md5(enc_wrd.strip()).hexdigest()
	    # print(word)
	    # print(digest)
	    # print(pass_hash)
	    if digest.strip() == pass_hash.strip():
	        print("password found")
	        print("Password is " + word)
	        flag = 1
	        break
	 
	if flag == 0:
	    print("password not in list")
```

Okay, guys, this brings us to the end of this “Ethical Hacking Using Python” article. This is one of the blogs in a long list of ethical hacking blogs that I have published. For more information regarding cybersecurity, you could check out my other blogs. If you have any doubts or queries regarding this particular article, leave a comment in the comments section below!