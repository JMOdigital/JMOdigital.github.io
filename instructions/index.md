---
layout: page
title: Author Instructions
class: 'post'
navigation: True
logo: 'assets/images/ghost.png'
current: instructions
---

### 1. Register a Github Account

Register for a free Github account [here](www.github.com).

Send your Github username to the JMO Digital Admin to be approved for access. Email: __contact@jmodigital.com__ 

Access the JMOdigital Github repository using [prose.io](www.prose.io). Login using your Github credentials. 

**Please do not modify any parts of this repository except the post you are working on.**

___

### 2. Write your post

Have a look at a sample post in the **_posts** folder of the Github repository. 

Posts should be written using *Markdown*. This is a shorthand formatting tool that will allow you to produce beautiful articles (like [this](../what-if-hospitals-ran-like-apple/)) with a basic text editor. 

Here is a link to a [Markdown cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).   

At the top of your post you need some **frontmatter**. This contains some important meta-data about your blog post such as author name, date, tags etc. 

Here is an example of the frontmatter: 
```
layout: post
cover: 'assets/images/cover6.jpg'
title: What if hospitals were run by Apple
date:   2015-01-01 10:18:00
tags: ideas bankstown
author: martin
categories: martin
navigation: true
disqus: true
```

##### Notes: 

- layout: should always be post
- cover: replace "cover6" with the name of your image. Put your image into the **/assets/images/** folder
- date: please obey the YYYY-MM-DD TIME format
- tags: these are the categories you want your post to be associated with e.g. your hospital name, *idea* if you want it to be on the ideas portal etc
- author: your **first name** - important so we can automatically match the article with your author profile
- categories: your **first name** 
- navigation: should always be true
- disqus: this relates to the commenting at the bottom of your post. You can disable this if you choose. 


Save your post as text file with the following naming schema: 
> 2015-10-10-nepean-jmo-wiki.md

Date - title
In .md format (Markdown)

Finally, upload your post into the **_posts** folder of the Github repo. 

___

### 3. Create your author profile

Add your author profile to the **_data/authors.yml** file. 

Please mimic the format of the existing authors:
```
-   name: Joe Bloggs
    email: joe@gmail.com
    nickname: your first name - **important** 
    bio: 'One sentence bio'
    location: 'Melbourne, Australia'
    url: your website (optional)
    image: your headshot (optional)
```

___
