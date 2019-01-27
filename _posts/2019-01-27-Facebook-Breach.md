---
layout: article
title: "What We Learned From The Facebook Breach"
date: 2019-01-27 17:00:00+0200
coverPhoto: https://sophosnews.files.wordpress.com/2018/10/fb-1200.png?w=780&h=408&crop=1
---

![](https://cdn.vox-cdn.com/thumbor/CdHv7c_X0_wQ1Yt4MI-rgZX27V4=/0x0:2040x1360/1200x800/filters:focal(857x517:1183x843)/cdn.vox-cdn.com/uploads/chorus_image/image/62607946/jbareham_180405_1777_facebook_0003.0.jpg)

Headlines continue to abound about the data breach at Facebook.

Totally different than the site hackings where credit card information was just stolen at major retailers, the company in question, Cambridge Analytica, did have the right to actually use this data.

Unfortunately they used this information without permission and in a manner that was overtly deceptive to both Facebook users and Facebook itself.

Facebook CEO Mark Zuckerberg has vowed to make changes to prevent these types of information misuse from happening in the future, but it appears many of those tweaks will be made internally.

Individual users and businesses still need to take their own steps to ensure their information remains as protected and secure as possible.

For individuals the process to enhance online protection is fairly simple. This can range from leaving sites such as Facebook altogether, to avoiding so-called free game and quiz sites where you are required to provide access to your information and that of your friends.

A separate approach is to employ different accounts. One could be used for access to important financial sites. A second one and others could be used for social media pages. Using a variety of accounts can create more work, but it adds additional layers to keep an infiltrator away from your key data.

Businesses on the other hand need an approach that is more comprehensive. While nearly all employ firewalls, access control lists, encryption of accounts, and more to prevent a hack, many companies fail to maintain the framework that leads to data.

One example is a company that employs user accounts with rules that force changes to passwords regularly, but are lax in changing their infrastructure device credentials for firewalls, routers or switch passwords. In fact, many of these, never change.

Those employing web data services should also alter their passwords. A username and password or an API key are required for access them which are created when the application is built, but again is rarely changed. A former staff member who knows the API security key for their credit card processing gateway, could access that data even if they were no longer employed at that business.

Things can get even worse. Many large businesses utilize additional firms to assist in application development. In this scenario, the software is copied to the additional firms' servers and may contain the same API keys or username/password combinations that are used in the production application. Since most are rarely changed, a disgruntled worker at a third party firm now has access to all the information they need to grab the data.

Additional processes should also be taken to prevent a data breach from occurring. These include...

• Identifying all devices involved in public access of company data including firewalls, routers, switches, servers, etc. Develop detailed access-control-lists (ACLs) for all of these devices. Again change the passwords used to access these devices frequently, and change them when any member on any ACL in this path leaves the company.

• Identifying all embedded application passwords that access data. These are passwords that are "built" into the applications that access data. Change these passwords frequently. Change them when any person working on any of these software packages leaves the company.

• When using third party companies to assist in application development, establish separate third party credentials and change these frequently.

• If using an API key to access web services, request a new key when persons involved in those web services leave the company.

• Anticipate that a breach will occur and develop plans to detect and stop it. How do companies protect against this? It is a bit complicated but not out of reach. Most database systems have auditing built into them, and sadly, it is not used properly or at all.

An example would be if a database had a data table that contained customer or employee data. As an application developer, one would expect an application to access this data, however, if an ad-hoc query was performed that queried a large chunk of this data, properly configured database auditing should, at minimum, provide an alert that this is happening.

• Utilize change management to control change. Change Management software should be installed to make this easier to manage and track. Lock down all non-production accounts until a Change Request is active.

• Do not rely on internal auditing. When a company audits itself, they typically minimize potential flaws. It is best to utilize a 3rd party to audit your security and audit your polices.

Many companies provide auditing services but over time this writer has found a forensic approach works best. Analyzing all aspects of the framework, building policies and monitoring them is a necessity. Yes it is a pain to change all the device and embedded passwords, but it is easier than facing the court of public opinion when a data breach occurs.

