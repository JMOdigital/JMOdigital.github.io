---
layout: post
cover: 'assets/images/automation.jpg'
title:  Automating primary care - tricks and tricorders
date: 2016-05-12 10:00:00
tags: ideas
subclass: 'post tag-ideas'
categories: 'martin'
navigation: True
logo: 'assets/images/ghost.png'
author: martin
---

> The Tricorder Prize is a high-profile challenge that draws on the popular imagination of an all-in-one diagnostic toolkit in the palm of a hand. These devices stand to be an ally for general practitioners. Their utility will be not so much in spot diagnoses as in longitudinal tracking of chronic diseases, offering intelligent, personalised advice to patients in between doctor’s visits. 

The Tricorder X-Prize is an international innovation challenge promising US$10 million to the team who can crack the elegantly elusive problem of the 'tricorder'. The tricorder is a device plucked from the realms of science fiction - a handheld health analyser originally featured in Star Trek which has the tri-functionality of sensing, computing and recording health. A little black box with a screen and detachable probe, the tricorder could sense vital signs, analyse bloodwork and thereby diagnose a range of medical conditions. Although it could send distress signals, the tricorder could not deliver treatment - it was a portable, easy-to-use diagnostic toolkit. 

Almost 50 years after this device appeared on television screens, the med-tech community has pounced upon it as a legitimate scientific goal. The $10m X-Prize was announced in 2011 and 7 teams are now in the running, with the winner to be announced in early 2017. The criteria have been laid down - the device must be able to diagnose the following 10 so-called 'Core Conditions':

* Anemia
* UTI
* Diabetes
* AF
* Obstructive sleep apnoea
* COPD
* Pneumonia
* Otitis media
* Leukocytosis
* Absence of core conditions

The 10th core condition - the absence of the other other 9 - is perhaps the most treacherous of them all if you read the fine print of the prize [guidelines](http://tricorder.xprize.org/about/guidelines). The gold standard that devices are held against to prove this null hypothesis is a very thorough workup indeed - test subjects undergo bloods, ECG, CXR, lung function tests, sleep apnoea tests and a brain MRI!

Incidentally, this list is actually a less ambitious version of what was proposed in 2011 when the prize first launched. There were originally 3 further conditions required: hepatitis A, tuberculosis and stroke. For bonus points, there is an extra set of 12 conditions to grapple with including pertussis, hyperthyroidism and HIV.

Devices must also be able to record 5 vital signs (blood pressure, HR and variability, temperature, respiratory rate and oxygen saturations), with a push towards continuous monitoring and upload to cloud storage. 

The 7 teams who remain in the running include 4 from the US and one each from Taiwan, Canada and India. The Canadian team [CloudDx](http://www.clouddx.com/) have put forward the VITALITI platform - an app-based analytics tool that syncs with multiple sensors including a wireless otoscope and a microphone for analysing breath sounds. VITALITI also has brightly-coloured test sticks for samples of finger-prick blood, urine and saliva. 

![VITALITI platform](http://www.clouddx.com/img/vitaliti_system.jpg "VITALITI platform")

[Scanadu](https://www.scanadu.com/), based out of the NASA Ames Research Center in Silicon Valley, have already gone to market with an early prototype, the Scanadu Scout, which will detect vital signs and provide basic recommendations for US$199.  They are now developing more sophisticated consumer health trackers called Scanadu Vitals and Scanadu Urine. Intriguingly, they already publish large-scale deidentified data through their [Global Body Map]( https://www.scanadu.com/globalbodymap/), foreshadowing the potential for real-time population analytics of health metrics. 

![Scanadu Scout](https://tctechcrunch2011.files.wordpress.com/2013/05/scanadu-scout.jpg "Scanadu Scout")

Then there is Boston's [DMI](http://www.dnamedinstitute.com/) team (DNA Medicine Institute), supported by the NIH and the Gates Foundation. They recently took out the smaller [Nokia Sensing X Prize](http://sensing.xprize.org/) with their rHEALTH device - a miniaturised pathology lab able to perform 22 tests on a single drop of blood using microfluidics and laser spectrometry.

Victory will be in the detail, but the skeleton of these ideas has already been sketched out. All of them involve a range of wireless sensing devices for vital signs and laboratory testing, linked to a software platform that recognizes trends and provides a diagnostic prediction.   

As these teams converge on an elegant solution, the question we have to grapple with is this: how would a tricorder-style diagnostic device actually interface with the delivery of healthcare? After all, it only solves one half of the equation: identifying a problem but not initiating treatment. One could argue that if you have diagnosed a UTI, taking the next step and suggesting appropriate antibiotic therapy for an uncomplicated patient is not a huge technical leap. But patients are rarely uncomplicated. And even if there are no objective medical complications, the psychosocial intricacies of healthcare mean that general practice and sensor technology will have to work hand in hand. 

This may not be such an odd coupling as some commentators, who prophesy the end of primary care with technological innovation, would have us believe. On the contrary, sensing technology might actually be the most useful tool for general practitioners in bringing efficiency to an increasingly overburdened primary healthcare system. 

Let's consider the most frequent presentations in a GP clinic. [Cooke *et al.*]( http://www.racgp.org.au/afp/2013/januaryfebruary/common-general-practice-presentations/) analysed almost 200,000 patient encounters from 2009-2010 using data from the [BEACH program](http://sydney.edu.au/medicine/fmrc/beach/) to produce a list of the problems most frequency managed by general practitioners. Numbers 1-10 were: 

1. Hypertension
2. Immunisations/vaccinations
3. Acute upper respiratory tract infection
4. Depression
5. Diabetes
6. Lipid disorders
7. General checkup
8. Osteoarthritis
9. Back pain
10. Prescription refilling

This list is notably different from the Tricorder Prize's top-ten list of acute conditions. The only item on this list that would typically require a tricorder-style spot diagnosis would be acute upper respiratory tract infection. (*NB. Although it may be possible to diagnose a large majority of URTIs based on a history of coryzal symptoms and certain relevant negatives, a rigorous diagnosis would also mandate examination of the pharynx, lymph nodes, conjunctiva, ear canals and breath sounds which is more difficult (although not impossible) to replicate with machines.*)

Apart from URTIs, almost all the other presentations relate to management of chronic conditions (with the exception of immunisations and general checkups). So the question of automating primary care is really one of automating chronic disease management. This is actually a domain where user-driven health tracking stands to be extremely useful. 

Imagine if the GP's decision about anti-hypertensive medications was informed by an accurate day-by-day trace of a patient's blood pressure over the last month, along with medication compliance, exercise levels and heart rate. We then move from trial-and-error medicine to tailored therapy. Imagine if the management of diabetes was informed by detailed BSL tracking, HbA1c levels and urine dipstick tests performed in a patient's home. Imagine if analgesia for chronic back pain was titrated in real time based on pain scores and side effect profile, just as it is for hospital inpatients. Imagine if cholesterol checks could be done in the household and subjects triaged to physicians accordingly. Primary care would be all the richer for it!

At the very minimum, these sensing platforms could make primary care decision-making asynchronous: rather than a patient physically attending the GP, browsing through tattered copies of Women's Weekly in the waiting-room, sitting face to face and leaving with some advice, that same advice could be delivered electronically via a GP who reviews the health data at a time that suits them. 

However we can go one step further. The picture that is really taking shape is of an automated concierge for chronic disease management in the home, advising on medications and lifestyle modifications in real time between visits to the GP. Of the 10 most common GP-managed problems, almost all could be tracked in a semi-automated fashion with the kind of devices competing for the Tricorder Prize.  

Primary care should not see these technologies as a rival, but as an ally. We are now at a critical fork in the road where we can build an ecosystem (including the regulatory and billing structures) to cater for semi-automated community medicine. And where private enterprises will be vying to get the automation right. As a medical profession, we should embrace these technologies and make them work for us, integrate them into our practice and extend our capacities, rather than undermine them as robotic competitors. 

