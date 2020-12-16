## Chilling Effects : Online Surveillance and Wikipedia Use

In June 2013, Edward Snowden revealed the extent of mass surveillance in the United States. As a result of this, the question arose : Did this news produce a "chilling effect"? In other terms, did Wikipedia traffic for articles on privacy-sensitive topics decrease after the “exogenous shock” of widespread publicity surrounding the surveillance programs in June 2013?

<img src="\images\surveillance.jpg">

### But what exactly is a "Chilling Effect" ? Wikipedia defines it as:

---

"In a legal context, the inhibition or discouragement of the legitimate exercise of natural and legal rights by the threat of legal sanction"

---

### How do we prove this chilling effect exists?

The approach was to analyse the number of views of certain English language Wikipedia articles. The list of articles was chosen from a list of keywords the U.S. Department of Homeland Security uses to track and monitor social media and the most pertinent ones were chosen through a crowdsorcing process.

Respondents were asked to indicate on a scale of 1 to 5 (1 being very unlikely and 5 being very likely):

- How likely they thought they would be in trouble if the U.S. government found out that they accessed information about the topic in question (Government Trouble Rating)

- How “privacy-sensitive” they viewed each topic as (in this case, 5 being highly sensitive and 1 not at all) (Privacy-Sensitive Rating)

- How likely they would be to delete the browser history on their computer after accessing information about the topic

- How likely they would avoid viewing or accessing information on the topic if they knew the Government was monitoring people’s activities online (Avoidance Rating).

The pageview numbers were collected over a thirty-two month period from January 2012 to August 2014, with June 2013 being the interruption. The goal was to use an interrupted time series (ITS) to plot the distribution of pageviews before and after this "interruption" and hopefully use it to prove that the knowledge of NSA surveillance caused a chilling effect on Wikipedia page views.

The pageviews of each article were aggragated by month producing this distribution.

**Add distribution with Hamas**

Upon further inspection, there were obvious outliers at month 11 (November 2012) and at month 31 (July 2014). After some research these spikes in pageviews coincided with spikes in pageviews for the "Hamas" article. This is due to incidents of unrest in the Middle East. The "Hamas" article proving to be an outlier, it was hence removed from the dataset.

The new and improved distribution of monthly pageviews look like this : 

**Distribution without Hamas**

We can see a large pageview "dropoff" in this distribution at the moment of Snowden's revelations and furthermore we can see that the overall trend of pageviews after June 2013 has a negative trend compared to the positive trend beforehand.

If we compare this with the pageviews of the most popular Wikipedia articles over the same period we can see the trend is severly different.

**avoir graph plus joli**




<img src="\images\wordcloud.jpg">
