---
layout: post
cover: 'assets/images/clouds.jpg'
title:  How to safeguard the privacy of Australian health data in the cloud
date:   2016-02-22 10:18:00
tags: data privacy
subclass: 'post tag-data tag-privacy'
categories: 'arran'
navigation: True
logo: 'assets/images/ghost.png'
author: arran
---

I once sat across from a doctor and stated that the only safe way to manage archival health data is in the cloud. As a consultant physician, I did not expect her retort to be *but what about the Patriot Act?* The Patriot Act is a now-replaced piece of American legislation that had far-reaching effects, with the [US Department of Justice laying claim to data stored by American companies?even overseas](http://www.theguardian.com/technology/2015/sep/09/microsoft-court-case-hotmail-ireland-search-warrant).

In Australia we are bound by myriad privacy acts spanning States, Territories and the Commonwealth, and no more resoundingly can their implications be felt than in the health community. And rightly so. We are privy to sensitive information, the disclosure of which can range from banal to destructive to the individual. The impact of even that which we see as trivial, through desensitising exposure, is highlighted by television such as *Embarrassing Bodies*.

My spy-wary conversationalist sparked a fervent exploration on my part. From a technical standpoint I was certain that prior encryption of health data would suffice for compliance with privacy legislation. But what about the Patriot Act?

Australian privacy requirements are based upon what are known as "privacy principles" - see this [quick reference guide](https://www.oaic.gov.au/agencies-and-organisations/guides/app-quick-reference-tool). Beyond the protection of data from unauthorised disclosure or modification, we have an obligation to adequately protect against loss of data. I argue that the most feasible means by which we can quantify the risk of data loss is in the cloud.

Cloud storage vendors are akin to insurance companies. They, respectively, spread the risk of data and financial losses across their pool of clients. When Amazon advertises 11-nines data integrity (1-in-100-billion probability of loss) it is founded in historical data much as that used by an actuary in determining your insurance premium [1]. Can any Australian hospitals provide this same level of precision?

Even with such motivation to migrate data to the cloud we are still met with security concerns. Borrowing from guidelines published by the Australian Signals Directorate - the agency tasked with our Government's information security - I have produced a [primer in cryptography with a focus on compliance with the specific wording of Australian privacy legislation](http://www.slideshare.net/ArranSchlosberg/data-security-in-genomics-a-review-of-australian-privacy-requirements-and-their-relation-to-cryptography-in-data-storage-57979838). Despite the genomic bent, it is relevant to every Australian tasked with the protection of health data.

___

*Disclaimer: I am not a lawyer and neither this post nor the publication should be construed as legal advice. The purpose of this text is to provide the reader with an adequate technical understanding of data security such that they can, in consultation with their lawyer, make informed decisions regarding data-management policy.*

<sub>*[1] Amazon Web Services Inc. "Amazon Simple Storage Service (S3) - Object Storage". Available from: https://aws.amazon.com/s3/. [Last accessed on 2016 Feb 7].*</sub>
