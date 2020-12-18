## Chilling Effects : Online Surveillance and Wikipedia Use

In June 2013, Edward Snowden revealed the extent of mass surveillance in the United States. As a result of this, a question arose: Did this news produce a "chilling effect"? In other terms, did Wikipedia traffic for articles on privacy-sensitive topics decrease after the “exogenous shock” of widespread publicity surrounding the surveillance programs in June 2013?

<img src="\images\surveillance.jpg">

### But what exactly is a "Chilling Effect" ? Wikipedia defines it as:

---

"In a legal context, the inhibition or discouragement of the legitimate exercise of natural and legal rights by the threat of legal sanction"

---

### How can we test for the existence of this chilling effect?

The approach was to analyse the traffic of certain English language Wikipedia articles. The list of articles was chosen using the government keyword lists, that the U.S. Department of Homeland Security uses to track and monitor social media and the most pertinent ones were chosen through a crowdsourcing process. More precisely, the articles used in the study were the ones associated with the keywords list "terrorism".

In order to verify the relevance of using these articles, respondents were asked to indicate on a scale of 1 to 5 (1 being very unlikely and 5 being very likely):

- How likely they thought they would be in trouble if the U.S. government found out that they accessed information about the topic in question (Government Trouble Rating)

- How “privacy-sensitive” they viewed each topic as (in this case, 5 being highly sensitive and 1 not at all) (Privacy-Sensitive Rating)

- How likely they would be to delete the browser history on their computer after accessing information about the topic

- How likely they would avoid viewing or accessing information on the topic if they knew the Government was monitoring people’s activities online (Avoidance Rating).

The pageview numbers were collected over a thirty-two month period from January 2012 to August 2014, with June 2013 being the interruption (month of the NSA/PRISM surveillance revelations). An interrupted time series (ITS), which is a series of measurements on the time axis, interrupted by a sudden event at some point in time, was used to plot the distribution of pageviews before and after this "interruption" and hopefully use it to prove that the knowledge of NSA surveillance caused a chilling effect on Wikipedia page views.

Upon further inspection, possible outliers were identified at month 11 (November 2012) and at month 31 (July 2014). After some research these spikes in pageviews coincided with spikes in pageviews for the "Hamas" article, due to incidents of unrest in the Middle East. There was a recorded 928,533 views for the page in November
2012, and 1,220,490 views in July 2014, both of which varied greatly from the mean number of view counts for the article across all 32 months (134,574 monthly views). The "Hamas" article proving to be an outlier, it was hence removed from the dataset.

You can see here Hamas' distribution:

<img src="\images\hamas.png">

Finally, in order to view the trend before and after the intervention month, a segmented linear regression is performed of the dataset. As you can guess, the regression is segmented in two parts: before and after June 2013.

This gives us the following result:

<img src="\images\figure_3.png">

We can see a large pageview dropoff in the pageviews at the moment of Snowden's revelations and furthermore we can see that the overall trend of pageviews after June 2013 has a negative trend compared to the positive trend beforehand.

In order to see if the dropoff and the tendencies are connected to our articles and not general to the Wikipedia viewing trend, the concept of "control group" is instaured. The pageviews of the most popular Wikipedia articles over the same period are ploted, in order to see if the tendencies found earlier are a general tendency ir directly linked to the articles.

<img src="\images\figure_5.png">

We can see the trend is severly different, hence it confirms the idea that this effect is due to the revelations of June 2013.

## Our extension: the effect of the GDPR

Questions can be asked as to the effect of liberty on our internet usage. Has the adoption of GDPR in 2016 induced european users to inform themselves about how to protect their own privacy? This was the question we asked ourselves.

In order to answer this question, we used Wikipedia articles relative to privacy and personal data protection in German, and the establishment of the General Data Protection Regulation (GDPR) in Europe to see whether these articles got any particular attention thanks to GDPR introduction

Would the knowledge that your privacy was better protected push you to seek out the how and the way of that protection? Let's look into it.

### Why German?

We decided to focus solely on German-language articles because the location of German speaking countries is mostly in Europe and therefore directly effected by GDPR. Let's confirm this theory by observing the geographical origin of the pageviews for de.wikipedia.org.

We can split this data into distinct origins:

- Germany
- Austria
- Switzerland
- Liechtenstein
- The rest of the European Economic Area (EEA)
- The rest of the world

<img src="\images\map_europe.jpg" width="400"/>

It is of note that Switzerland is not part of the EEA; however, since it is landlocked and all of its neighbours EEA members, and since GDPR-compliance is mandatory for selling digital services within the EEA, we can safely consider Switzerland to have been strongly impacted by GDPR too. It is also of note that the UK was included in this analysis as it is still considered as being part of the EEA in 2020.

We now plot the 2020 de.wikipedia.org pageviews with respect to these groups.

<img src="\images\german2020.JPG">

An argument could be made that coronavirus has upset so many things in 2020 that perhaps it altered the pageview origins as well. So let's do the same analysis for 2019 de.wikipedia.org pageviews.

<img src="\images\german2019.JPG">

As we can see both graphs as extremely similar and prove our hypothesis on the origin of German-language pageviews; they come almost entirely from European countries, countries that are effected by GDPR.

Let's delve further into our German article analysis...


### Data Collection

We started by collecting possible Wikipedia articles that could be of interest to the problem. We did this by simply visiting the Wikipedia page for "General Data Protection Regulation" and creating a list of all the referenced articles it contained (links in blue).

<img src="\images\GDPR.jpg">

Since this list can contain articles directly correlated with the subject, as well as very general articles, a ranking had to be done in order to select our article set. Once we had this list compiled, we asked thirteen participants to rank the pages on the question "Which of these Wikipedia articles would you most likely consult to inform yourself on the protection of your personal data online?". The ranking was from 1 to 5, 5 being "Very likely" and 1 "Not at all likely".

From all of the available articles we only retained those with an average score of 3 or higher, thus resulting in a dataset of 26 articles. We chose the cut-off score of 3 because this gave us a similar number of articles to the "chilling effect" dataset and an average score of 3 seemed like an acceptable rating of interest. Some of these did not have data through the whole period of time (for example because created later), so we had a final set of 22 articles.

<img src="\images\wordcloud.jpg">

### Result

To see if we can observe an increase in interest regarding online privacy issues after the establishment of the GDPR, we use the same technics as in the paper: compute and plot the trends. We got the following distribution

<img src="\images\distribution.jpg">

Here we can see that there seems to be outliers. Indeed, after research we found two articles containing months that were outliers: "European Union" and "Iceland". Let's plot their pageviews.

<img src="\images\distribution_iceland.jpg">

Once we remove these outliers we can visualise our data more clearly.

<img src="\images\distribution_cleaned.jpg">



