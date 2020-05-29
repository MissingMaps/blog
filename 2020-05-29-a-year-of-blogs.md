---
layout: post
title: "'Human Centered Design to drive the development of baseline health facility data with Healthsites – A Year of Blogs – May 2020"
postID: a-year-of-blogs-may2020
category: blog
banner: https://arcmaps.s3.amazonaws.com/share/blog-pictures/missingmaps-blog_20200529_photo1.png
date: 2020-05-29
author: Mark Herringer
excerpt: "Gathering an open, global dataset for healthcare data is something that healthsites.io is passionate about."
published: true
tags: [healthsites, Year-of-Blogs]
permalink: /blog/:year/:month/:day/:title/
lang: en
---


# Human Centered Design to drive the development of baseline health facility data with Healthsites – A Year of Blogs – May 2020

<figure>
<img src="https://arcmaps.s3.amazonaws.com/share/blog-pictures/missingmaps-blog_20200529_photo1.png">
<p class="caption"> [Lamine Ndiaye](https://twitter.com/lamineyasey/) Mapping health facilities in Saint Louis, Senegal</p>
</figure>

Gathering an open, global dataset for healthcare data is something that healthsites.io is passionate about. Deciding how and what to gather for such a global dataset is a challenge. There are many stakeholders and many aspects of a given facility that could be collected. Healthsites is embarking on this with a user centered design approach. Our goal is to build a platform that collates data that is relevant to the questions that healthcare facility users need answered. In this article we concentrate on Human Centered Design and how it will help us to build a platform that meets the needs of the people using it.

We want you to share user stories.

# What is user Human Centered Design?

A Human Centered Design approach to design drives the requirements and functionality of a platform based on the direct needs expressed by its users. We can express these needs in simple sentences that share a common structure : 

### As a <..........> I would to <..........> so that I can <..........>

Let’s look at some tangible examples, one from chatting with an expectant mother and one from a conversation with a civil servant working for a health ministry:

As a pregnant mom expecting twins I would like to know where the nearest **emergency care facility** is so that I can  plan for potential complications during childbirth.

As a ministry of health data administrator, I want to know **how long it takes** citizens to get to health facilities so that I can optimize access to health care.

As a ministry of health data administrator, I want to know the geographic **coordinates of health facilities** so that I can perform a spatial analysis.

As a PATH health data administrator, I want to know where the **operational clinics** are so that I can plan a vaccination rollout campaign.


Collating these stories from users of the platform for different persona’s in the healthcare environment provides us with an understanding  of what problems need to be solved and what data are needed to solve them.

### Deconstructing the user stories

When we deconstruct user stories, we can understand what kind of information is needed to support the story. Taking our examples above we can see:

**Who | What | Why**
------------ | ------------- | -------------
Expectant mother | Emergency care | plan for potential complications during childbirth
Ministry of Health data administrator | how long it takes citizens to get to health facilities | optimize access to health care
Ministry of Health data administrator | know the geographic coordinates of health facilities | perform a spatial analysis
PATH health data administrator | know where the operational clinics are | plan a vaccination rollout campaign

In 2018 the Healthsites project decided to switch to a data model built almost entirely upon the OpenStreetMap.org (OSM) platform. As well as leveraging the power of the world’s most amazing open data project, this approach also introduces constraints in the design of our platform and how we can mobilise data to meet the needs of our users that emerge through their stories. The constraints are the normative guidelines that the OSM project places on the capture of data for any feature (healthcare or otherwise). For example, it is difficult to introduce new concepts on the platform which is shy of ‘concept proliferation’, and considerable effort needs to be made to understand the existing concepts within the OSM tagging system. So, to meet the needs of people interested in healthcare data, we need to ‘map’ concepts. Taking the ‘what’ column from the above table, we can identify which attributes in the Healthistes schema are the most important to focus on.

**No. | Key | Value | Description**
------------ | ------------- | ------------- | -------------
1|amenity|clinic, doctors, hospital, dentist, pharmacy|For describing useful and important facilities for visitors and residents
2|healthcare|doctor, pharmacy, hospital, clinic, dentist, physiotherapist, alternative, laboratory, optometrist, rehabilitation, blood_donation, birthing_center|A key to tag all places that provide healthcare (are part of the healthcare sector) 
3|healthcare:speciality|biology, blood_check, clinical_pathology, diagnostic_radiology, medical_physics, medical_engineering, radiology|A key to detail the special services provided by a healthcare facility. To be used in conjunction with the 'healthcare=*' tag. For example 'healthcare=laboratory', and 'healthcare:speciality=blood_check'
4|name|name of health facility|The primary tag used for naming an element
5|operator|name of operator|The operator tag is used to name a company, corporation, person or any other entity who is directly in charge of the current operation of a map object
6|source|source of data|Used to indicate the source of information (i.e. meta data) added to OpenStreetMap


# Complete


No|Key|Value|Description
------------ | ------------- | ------------- | -------------
1|amenity|clinic, doctors, hospital, dentist, pharmacy|For describing useful and important facilities for visitors and residents
2|healthcare|doctor, pharmacy, hospital, clinic, dentist, physiotherapist, alternative, laboratory, optometrist, rehabilitation, blood_donation, birthing_center|A key to tag all places that provide healthcare (are part of the healthcare sector)
3|healthcare:speciality|biology, blood_check, clinical_pathology, diagnostic_radiology, medical_physics, medical_engineering, radiology|A key to detail the special services provided by a healthcare facility. To be used in conjunction with the 'healthcare=*' tag. For example 'healthcare=laboratory', and 'healthcare:speciality=blood_check'
4|name|name of health facility|The primary tag used for naming an element
5|operator|name of operator|The operator tag is used to name a company, corporation, person or any other entity who is directly in charge of the current operation of a map object
6|operator:type|public, private, community, religious, government, ngo, combination|This tag is used to give more information about the type of operator for a feature
7|addr:full|full address|Used for a full-text, often multi-line, address for buildings and facilities
8|contact:phone|phone number|The contact tag is the prefix for several contact:* keys to describe contacts
9|operational_status|operational, non_operational, unknown|Used to document an observation of the current functional status of a mapped feature
10|opening_hours|days/times of opening|Describes when something is open or closed. There is a specific standard format for this data https://wiki.openstreetmap.org/wiki/Key:opening_hours/specification
11|beds|number of beds|Indicates the number of beds in a hotel or hospital
12|staff_count:doctors|number of doctors|Indicates the number of doctors in a health facility
13|staff_count:nurses|number of nurses|Indicates the number of nurses in a health facility
14|healthcare:equipment|ultrasound, mri, x_ray, dialysis, operating_theater, laboratory, imaging_equipment, intensive_care_unit, emergency_department|Indicates what type of speciality medical equipment is available at the health facility
15|dispensing|yes, no|Whether a pharmacy dispenses prescription drugs or not. Used to add information to something that is already tagged as amenity=pharmacy
16|wheelchair|yes, no|Used to mark places or ways that are suitable to be used with a wheelchair and a person with a disability who uses another mobility device (like a walker)
17|emergency|yes, no|This key describes various emergency services
18|insurance:health|none, public, private, unknown|This key describes the type of health insurance accepted at the healthsite
19|water_source|well, water_works, manual_pump, powered_pump, groundwater, rain|Used to indicate the source of the water for features that provide or use water
20|electricity|grid, generator, solar, other, none|Used to indicate the source of the power generated
21|url|url of source data|Specifying a url related to a feature, in this case the wiki page if it is linked to an organised mapping effort, both through surveying and importing
22|source|source of data|Used to indicate the source of information (i.e. meta data) added to OpenStreetMap

https://wiki.openstreetmap.org/wiki/Global_Healthsites_Mapping_Project

# Open data policy development
In this context stakeholders in the health cluster can define open data policies that support these user stories and improve base line health facility data.

In a three day workshop ‘ Developing a Strategic Agenda around Outbreak and Humanitarian Data Collection and Analytics’ held at the Wellcome Trust between 20-22 March 2019 the following recommendations were established:

* Cross functional teams need to be part of the conversation and include field staff
* Lack of a labour market to retain trained staff is a significant threat to sustainability
* Countries require the data infrastructure, human resources and computational capacity to predict and model both climate risks and mitigation strategies
* Timely, standardised, shared data
* Improved focus on 'climate induced humanitarian emergencies'

You can read more about the workshops findings here [A joint way forward in developing tools, methods, training and dissemination with a consortium of global partners](https://www.tephinet.org/workshop-on-%E2%80%9Cdeveloping-a-strategic-agenda-around-outbreak-and-humanitarian-data-collection-and) 

The COVID-19 pandemic is generating new user stories. These need to be understood and communicated.

As both TB and COVID-19 share similar clinical presentation (cough, fever, shortness of breath etc.) and are transmitted through respiratory droplets and aerosols, a combined strategy needs to be applied. This would utilise resources effectively while providing both short term and long term benefits. - [Impact of COVID-19 intervention on TB testing in South Africa.](https://www.nicd.ac.za/wp-content/uploads/2020/05/Impact-of-Covid-19-interventions-on-TB-testing-in-South-Africa-10-May-2020.pdf)

## Healthsites invites local practitioners to [make contact](https://healthsites.io/contact/) and help define user stories that drive the development of baseline health facility data where it is needed most.

The Healthsites team  
[https://healthsites.io/](https://healthsites.io/)  
[https://twitter.com/sharehealthdata](https://healthsites.io/)
