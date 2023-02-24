# UNICRI-Decode-CW
![REDUCED_FOR_GIT_UNICRI-2022-Jindrich_Karasek-Decode-Cognitive-Warfare](https://user-images.githubusercontent.com/105706451/221148351-fe007ed4-b065-4fd4-b8ee-424e7728d999.jpg)

![REDUCED_FOR_GIT_UNICRI-2022-Jindrich_Karasek-Decode-Cognitive-Warfare (1)](https://user-images.githubusercontent.com/105706451/221148537-8fbda711-cb25-41d1-a5fc-8f55da280e4d.jpg)

If I had only one slide to show you
 and one message to share -  
it is that there are already tools and open source libraries that enable you to do fairly significant portion of cognitive warfare analysis. 

My goal is to show you how to use some of them, based on my own field experience.

I will mention few relatively simple tricks, that can be the base for building your own “in house” competence right away.
 
Purpose of this setup is to lower the entry barrier for the government analysts.
It should help you to quickly assess the information landscape and have the stable and consistent methodology for intelligence collection, analysis and dissemination.

![REDUCED_FOR_GIT_UNICRI-2022-Jindrich_Karasek-Decode-Cognitive-Warfare (2)](https://user-images.githubusercontent.com/105706451/221148771-3942526a-228f-4574-9494-673fbc494ff4.jpg)

The idea of the Killchain is to split the activity of the adversary to separated consecutive phases. Interrupting at certain point would block the adversary to continue and they need to start from the beginning, differently.

Recon - finding the cracks is all about finding the vulnerable entities in information landscape. May it be groups of individuals, discussion forums, organisations and so on.
Build - Knowing the cracks where to strike, adversary prepares the environment, builds and activates personas.
Seed - Using activated personas from previous stage, adversary seeds the first malicious content to begin with the influence operation.
Copy - Sharing, retweeting, making the content more available for next stage..
Amplify - Using all possible means to make the content as much visible as possible. So it looks like that it is the only truth there is.
Control - Drive the target audience toward the final stage..
Effect - Target audience is confused, does not believe official information, institutions, each other. Crowd like this is easily controlled, manipulated or oven used to kill other people or remove the governments.

![REDUCED_FOR_GIT_UNICRI-2022-Jindrich_Karasek-Decode-Cognitive-Warfare (3)](https://user-images.githubusercontent.com/105706451/221148846-967057e3-5e88-406b-9d92-23736a5388c0.jpg)

![REDUCED_FOR_GIT_UNICRI-2022-Jindrich_Karasek-Decode-Cognitive-Warfare (4)](https://user-images.githubusercontent.com/105706451/221148879-2f3b52a9-cb91-4f36-819f-eb0611864446.jpg)

One of the tasks is so called topic modeling.
Plain text, created under certain context of the intelligence, is taken to create a so called corpus and this is further analyzed with ML algorithm to learn the meaning of the text without the need of reading it.
To demonstrate its advantage, I chose to analyze the corpora based on dataset collected during my analysis of so called “Incel” world.

Being incel means that you claim to live in an involuntary celibacy. This community is full of troubled problematic personalities and it is being very actively used by various adversaries to take advantage on them for their own agenda.
On the slide, you see  three different forms of visualization of the topics, being discussed within the community.
Note the cluster close to the center of the intertropical distance map - It is a proof that the community was being driven by the adversary.
It is the personas used to “fill in the gap” in the discussions to employ the narratives set by the adversary.

![REDUCED_FOR_GIT_UNICRI-2022-Jindrich_Karasek-Decode-Cognitive-Warfare (5)](https://user-images.githubusercontent.com/105706451/221148990-c226f888-87b3-4d52-ad83-73718b19c6ff.jpg)

![REDUCED_FOR_GIT_UNICRI-2022-Jindrich_Karasek-Decode-Cognitive-Warfare (6)](https://user-images.githubusercontent.com/105706451/221149036-6c583c10-7413-4c0a-9a2b-37a488f702a2.jpg)

Next method I need to mention is so called “named entity recognition”. 
Take the example from the slide - there is a short text and the list of detected entities.
Note that we need to know which language model to use in advance. Therefore, input data for this method has to be sort by the language first.
Knowing the entities mentioned in the text is again extremely useful and with the help of some annotation tools you can also train or update current model to detect new entities.

![REDUCED_FOR_GIT_UNICRI-2022-Jindrich_Karasek-Decode-Cognitive-Warfare (7)](https://user-images.githubusercontent.com/105706451/221149122-b19bdcd6-5c27-4180-b177-345ed53b0ddf.jpg)

In this notebook you will take the twitter dataset based on hashtag “zelenskywarcriminal” because we can expect strong sentiment present in the tweets and you will extract the sentiment, keywords and named entity to a table.
![REDUCED_FOR_GIT_UNICRI-2022-Jindrich_Karasek-Decode-Cognitive-Warfare (8)](https://user-images.githubusercontent.com/105706451/221149323-9eebe257-5437-4d5a-88fd-811859e949c4.jpg)

The cognitive warfare works only as long as it triggers strong emotions. 
Well, fortunately this is also possible to detect.
To do so, you need to use proper language model and somewhat powerful machine.
Sentiment is represented numerically and you can compute the sentiment for short spans of text like the tweets about the War in my example.
Or the comments, short messages. 
It actually makes more sense than calculation of the sentiment for a whole book or a website at once.
Because in most use cases, you care about sentiment expressed to something particular and not just the sentiment of whole text body, 
which would be composed from addition of all the detected sentimental expression in the corpus of the text.

![REDUCED_FOR_GIT_UNICRI-2022-Jindrich_Karasek-Decode-Cognitive-Warfare (9)](https://user-images.githubusercontent.com/105706451/221149403-0f096b78-7aea-46a9-94ba-2182d9fc7f16.jpg)

In this case you may try to use twitter public API to download data from particular twitter user.
It is valid for monitoring influential personas to monitor the narratives they are spreading.

![REDUCED_FOR_GIT_UNICRI-2022-Jindrich_Karasek-Decode-Cognitive-Warfare (10)](https://user-images.githubusercontent.com/105706451/221149732-5005ac44-d194-4f95-ad65-a9bcec8981e9.jpg)


Lastly - something that I used to hate back in the time I was a school kid is the analysis of parts of the speech.
This is however crucial for us to be able to generate so called semantic graphs.
To properly analyze influence operations in cyber world, you need to be able not only detect entities and related sentiment, but also broader context of the entities and this is when the Parts of the speech detection enters the game.

![REDUCED_FOR_GIT_UNICRI-2022-Jindrich_Karasek-Decode-Cognitive-Warfare (11)](https://user-images.githubusercontent.com/105706451/221149500-5d33d227-a22a-4133-8a18-391958373b2f.jpg)

Combined altogether - here is a result of text analysis. Dataset is based on the book - Silmarillion.

I chose that book for the following reasons:

It is reasonable sized,  the language is the textbook english and I know it pretty well to spot oddities.
What's even more important - Silmarillion universe is a fiction.
With the usage of ML I wanted to be cautious since I don’t have so many options to validate the  outputs. 
So I used this awesome made up universe to verify that entities are detected properly, sentiment fits and even the names of the places are recognized as the places and not people.
And it worked!

See for yourself - if you know a bit the stories, you can understand the semantic graph right away. You see the strongest ties between the entities and by the color you can also tell the sentiment interval they have with each other.
The smaller picture is a view of the raw dataset before post processing.

The outer circle is just a noise. Sometimes the spam.

 The middle circle is not a noise - but it is mostly composed from smaller isolated graphs - this would appear in every dataset.


The core is on the other hand the place, where you can find the most of the cognitive warfare. The idea is, that these two visual cluster allow for topological analysis of quite complex graphs to determine, what is realization of freedom of speech and what is already the cognitive warfare.
![REDUCED_FOR_GIT_UNICRI-2022-Jindrich_Karasek-Decode-Cognitive-Warfare (12)](https://user-images.githubusercontent.com/105706451/221149911-163a13d9-e9a6-4ca3-a334-d0bceb698f32.jpg)

Websites : Angelic hoaxes, keyword per URL graph visualisation.
The threat actor created number of websites, that seemed to discuss the mysticism related to the angels, from the Christian, Judaism and Islamic point of view.
Closer look shows however, that in fact it was a part of the influence operation with antivax and anticovid narratives.

If you guess the microchips and 5G hoaxes, you are correct!
![REDUCED_FOR_GIT_UNICRI-2022-Jindrich_Karasek-Decode-Cognitive-Warfare (13)](https://user-images.githubusercontent.com/105706451/221150020-96fa6b79-1127-49b1-9ca7-0dc4dbd2fe19.jpg)

And finally, see the same method applied to real dataset from the threat hunting that I did for my country.
It is post processed graph to only show the core - the real manifestation of the cognitive warfare in my country last couple years.
You can see mentioned entities and their ties to various narratives. 
When graphed altogether like this, you have the estimate of activity groups and can model the strategic communication needed to neutralize them.
Knowing the data sources - undisclosed on purpose - you may even derive the attribution to nation states behind the operation

![REDUCED_FOR_GIT_UNICRI-2022-Jindrich_Karasek-Decode-Cognitive-Warfare (14)](https://user-images.githubusercontent.com/105706451/221150129-1618f817-77d7-42d6-a24c-d79688a62287.jpg)

This part of the code will quickly show you how to extract data from an email message.
Second part of the code will help you create a graph structure similar to the one from the picture.

![REDUCED_FOR_GIT_UNICRI-2022-Jindrich_Karasek-Decode-Cognitive-Warfare (15)](https://user-images.githubusercontent.com/105706451/221150174-5c40cd86-1da2-4522-b21e-5a1ba543d6ec.jpg)

With previously mentioned techniques - I would like to introduce my research project or framework, if you wish, called Eolas.
The name means knowledge or information itself and suggest that the base of this work is in knowledge graphs.

So what does it do:
In semi automated way it can be used to collect the data from various resources, turn them into the plain text and analyze that/
Goal of this project is to introduce stable and objective methodology to assess the campaigns of possible influence operations in cyberspace.
By that, I plan to improve legislation and monitoring capabilities.

Given the specific context and threat scape, Eolas also give additional insight of Advanced persistent threats and manipulators.

![REDUCED_FOR_GIT_UNICRI-2022-Jindrich_Karasek-Decode-Cognitive-Warfare (16)](https://user-images.githubusercontent.com/105706451/221150254-e0a86080-8925-4929-8962-d6f2c44348ba.jpg)

The blueprints of the Eolas itself. Let's split the process flow to four stages:

In first stage - monitoring - it spots the cracks in the information space.
Be it online forums, telegram groups, known manipulative websites or tweets.

Data mining phase:
It is possible to spot events like topic testing, reputation building for the personas, initial drops, see what is most shared content.

Next, data processing:
This includes building of semantic graph, clustering the infrastructure and entity link analysis.

Output:
With knowledge like this, it is possible to generate a reports, alerts or briefs for strategic communication.

It uses all the methods from previous slides. It has its own infrastructure and I am not able to share the stable version at the moment. 
It is, because I work on something much more powerful!

![REDUCED_FOR_GIT_UNICRI-2022-Jindrich_Karasek-Decode-Cognitive-Warfare (17)](https://user-images.githubusercontent.com/105706451/221150435-0904bf93-fd1c-4e79-8210-0025ecb3b80d.jpg)

Notable part of data mining capabilities in project Eolas is based on various kinds of crawlers.
During the crawling operations, I have found out that certain manipulative website employed say “anti research” measures, including:

Blocking the visitors based on location or IP.
They blocked requests with default or non browser user agents.
They cut the connections taking too long or being too frequent.
Automated content generation to create a rabbit hole for a crawler to drown it with junk data.
Automated pages generation to exhaust the capacity of the crawler by setting the huge number of pages to the crawling queue.

Hack backs - “coincidental” server failures after crawling or scanning certain websites or infrastructure.

![REDUCED_FOR_GIT_UNICRI-2022-Jindrich_Karasek-Decode-Cognitive-Warfare (18)](https://user-images.githubusercontent.com/105706451/221150538-21b79e48-da51-46d5-b026-886c1fe97757.jpg)

Eolas evolved to something much broader.
We have introduced the cognitive science to the design and this gives us prospect not only to analyze the cognitive warfare from the cyber threat hunting point of view, but also process the data to generate cognitive antidotes.
These antidotes would address particular narratives on lower levels of human mind to either neutralise the initial adversary emotions, or to turnt he victim attention to something else.

![REDUCED_FOR_GIT_UNICRI-2022-Jindrich_Karasek-Decode-Cognitive-Warfare (19)](https://user-images.githubusercontent.com/105706451/221150608-6d5995f6-d060-4230-b667-26eb0304dfc7.jpg)


![REDUCED_FOR_GIT_UNICRI-2022-Jindrich_Karasek-Decode-Cognitive-Warfare (20)](https://user-images.githubusercontent.com/105706451/221150635-61cbe91c-a9bd-415b-9a1c-40fb7b3f6602.jpg)



