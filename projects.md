---
layout: default 
title: Projects
permalink: /projects/
---

<h1>Past and current projects</h1>
Some neat stuff that I've worked on, am currently working on, or have contributed to, in a team or individually.


1. [Indian Village Satellite Imagery and Energy Access Dataset](https://figshare.com/articles/Indian_Village_Satellite_Imagery_and_Energy_Access_Dataset/5552743) - A supervised-learning dataset compiled in summer 2017 in the Data+ program that contains detailed features for every village in the Indian state of Bihar, including satellite imagery, political boundaries, lights at night imagery, rainfall and vegetation indices and electrification rate approximations. In the current academic semester, I'm working to develop classifiers using this data to be able to predict electrification rates at scale. 

- Read more about our work: [Research Poster](https://energy.duke.edu/sites/default/files/images/Poster_Electricity_Access.pdf), [Summary Presentation](http://bigdata.duke.edu/sites/bigdata.duke.edu/files/site-images/Team2ExecSummSlides_0.pdf?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_treasury%3BA0Ft2JohR%2Fmgw72V4%2BXi2Q%3D%3D), [Duke Research Magazine Feature](https://researchblog.duke.edu/index.php/2017/08/01/mapping-electricity-access/)

2. [Power Plant Satellite Imagery Dataset](https://figshare.com/articles/Power_Plant_Satellite_Imagery_Dataset/5307364) - A supervised-learning dataset of satellite imagery of powerplants agglomerated in summer 2017 for potential usage in training computer vision and machine learning models or applications. Open-source dataset has been published on Figshare. Technologies used included Python/NumPy/SciPy, ArcGIS. 

3.	[Politiquette](https://github.com/rahulgs12/politiquette) – A Chrome browser extension displaying on-hover interest group ratings for US senators on inequality issues, developed backend API-like functionality for the extension in Flask, Python, HTML/CSS/JS 

4. [Biology IT Inventory](http://bioinventory.herokuapp.com/) - A web platform and accompanying REST API built using Django, the Django REST Framework and PostgreSQL for keeping track of loaner equipment inventory of Duke's Biology IT helpdesk. [GitHub](https://github.com/shamikh-mill/bio-inventory)

5. [Hitchecker](https://github.com/tn74/MTurkAnnotationTool/blob/master/ASCRIPT_hit_checker.py) - A research tool and Python program for crowdsourced data review that uses the Amazon Mechanical Turk API to allow researchers/Turk users to review image labels and annotations received for their crowdsourced Human Intelligence Tasks (HITs). Built in summer 2017 as part of an open-source end-to-end web [platform](https://github.com/tn74/MTurkAnnotationTool) for receiving and reviewing responses on Mechanical Turk for construcing image-related training datasets. Reduced the time needed for paying workers as well as reviewing the crowdsourced data for human error, random or systematic.

6. [Duke Registration Enhancer](https://chrome.google.com/webstore/detail/duke-registration-enhance/ahlkcnepemhengifaokogcgbfggpkjmk) (Contributor to open-source project) - Duke Registration Enhancer is a Google Chrome extension that provides front-end visual enhancements to Duke University's online class registration platform. I modified an instructor lookup feature that made an excess amount of requests to the RateMyProfessors site to pull rating information by implementing a request-free link generation algorithm in JavaScript. [GitHub](https://github.com/williamyeny/duke-registration-enhancer)

7. [DAMUN Website](http://damunconference.org/) - Created new conference website for Model UN school organization using WordPress CRM, website was awarded grant from the [UN Foundation](http://www.unfoundation.org/) after an employee there found our new website. 

8. [Video Tutorial Series](https://www.youtube.com/user/computerpowerguide) - maintained YouTube channel of HD tutorials on
computer software and graphic design, accumulated 185,000+ video views over the years. 

9. IB Extended Essay in History: [The Effect of Civil Service Examinations on the Great Divergence in Late Dynastic China](http://shamikh-mill.github.io/ee.pdf) - Research paper written for the IB program in my senior year of high school examining a question I had wondered about since 10th grade- how did China's civil service examinations affect its macroeconomic growth over time, and did it have anything to do with [the Great Divergence](https://en.wikipedia.org/wiki/Great_Divergence)?


Posts
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{site.baseurl}}{{ post.url }}">{{post.title}}</a>
    </li>
  {% endfor %}
</ul>
