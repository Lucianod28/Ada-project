---
layout: page
title: Radek test
---

# Spending trends over time

We analyze how much people spend on shopping and how that value changes over time.

First we compute the mean household spending each week and see how it looks over time. It seems there is an overall rising trend.


![svg](Story_PartRadek_files/Story_PartRadek_7_0.svg)


* There is a high deviation between subsequent weeks but we can see that the sales are overall increasing over time. The linear regression shows a rising tendency.

* The big drop in the last week is most likely caused by the fact that this week is underrepresented (it doesn't contain the last day).


![svg](Story_PartRadek_files/Story_PartRadek_11_0.svg)


As week by week data has very high variance (which is likely caused by for example some people doing big shopping only every two weeks etc.), we look at the monthly spending.

The plot is much smoother and we can indeed see an increasing trend, especially at the very beginning (in the first half a year). After half a year the trend seems to still be rising, however it slows down a lot in comparison to the first months.

It is important to note how we should understand the data we have: we have sales data for a specific set of stores. The fact that we see an increase in spending over time what we really see is increase in store's sales. It is possible that it is due to the people startin o spend more money, but it is equally possible that they are spending the same amount, but choosing the stores we have access to more frequently instead of other stores that are not in this database. In fact the big rise in the first half a year could be explained by the store starting a marketing campaign - the small sales in the beginning could mean new customers starting to sometimes go to this stores and the rapid increase could be the result of them starting to choose it more and more often over other stores due to marketing. The slowdown afterwards may be due to saturation - most interested customers already have started to frequent these stores often and they don't change their habits that much anymore.


![png](Story_PartRadek_files/Story_PartRadek_14_0.png)


Looking at overall sales in all the shops makes the hypothesis from above even more likely - as we can see both plots are very similar. It seems that the shop chain was indeed gaining popularity very rapidly in the first 5-6 months, likely due to effective marketing.

## Individual trends

However people are not a namelss mass but a group of individuals. The mean household spending seems to be rising, but does that mean that all the people are spending more and more? Let's find out.

    /home/radeusgd/Anaconda3/envs/ada/lib/python3.7/site-packages/tqdm/std.py:651: FutureWarning: The Panel class is removed from pandas. Accessing it from the top-level namespace will also be removed in the next version
      from pandas import Panel


We now try to fit a Linear Regression model to the weekly spending of each household. The fitted line represents a 'trend' in the spending of the household - if the line is going upwards it means the household is spending more and if it is downwars the household is likely to started saving. A horizontal line means the spending stays more or less the same.

We will compute a percentage spending change - we fit the line to weekly spending (to avoid the high variance, the line is an approximation of a long term tendency) and assume the line's height in the first week is the starting value and its height in the last week is the final value and compute the percentage difference between the two.


    HBox(children=(IntProgress(value=0, max=2500), HTML(value='')))


    



    HBox(children=(IntProgress(value=0, max=2500), HTML(value='')))


    


We drop some extreme outliers to see the data in more detail. We have checked a random sample of the outliers and it seems it's mostly just caused by households that did very few transactions which makes the trend approximation very imprecise.


![png](Story_PartRadek_files/Story_PartRadek_27_0.png)


The absolute spending trend is just the coefficient of the linear trend - it is very dependent on the initial value. If someone was spending 200k in the beginning and in the end they are spending 210k, the coefficient would be the same as in the case someone was spending 10k and started spending 20k, but in fact these changes are drastically different (5% vs 100% increase).

That is why we will now analyse the percentage change described earlier - it is a better metric in terms of habits. Because a 2x is different from a 5% change.




    3.0



Only 3% of samples are extreme outliers, so we just drop them to make the histograms more readable. They are likely caused by households doing very few transactions and the trend approximation being imprecise with a small number of samples.


![png](Story_PartRadek_files/Story_PartRadek_32_0.png)





    32.453319262364886



A positive value means the spending has been increased - for example 100% means the spending is now twice as at the beginning, 0% means no change and -50% means the spending has decreased by 50% since the beginning.

Values smaller then -100% may look suspicious - what they represent is samples where there wasn't too much data so the approximated spending trend is indicating that at the end of the period they would be spending negative amounts which is of course illogical.
We can however treat these values just as big negative values, because these customers were spending much less over time.

What can be read from this histogram is that there more people who have an increase in spending than those who have a decrease. So our initial intuition was right - most people do spend more money in these stores. The average spending increase is 32%.

There are however lots of people that are spending less as well.


![png](Story_PartRadek_files/Story_PartRadek_35_0.png)





    61.53846153846154



The majority of people (who are saving) have decreased their spending by less than 50%




    (1252, 1170)




![png](Story_PartRadek_files/Story_PartRadek_40_0.png)





    536



Among people who are spending more (the overall majority), most of them are spending only slightly more, but there are minorities that are spending even 4x as much as before.

## Spending on days of week


![png](Story_PartRadek_files/Story_PartRadek_46_0.png)


* It is only a hypothesis, but it seems that 1 = Monday indeed, as the last two days get higher spendings and people tend to go shopping on the weekends (at least in countries when most shops are open on Sundays, but if this shop was closed altogether it would have 0 sales or small sales in only specific shopping points, which would be clear from the plot).

* So we can conjecture that 1 = Monday, 7 = Sunday and people do most sales on the weekend (which seems reasonable as they have more time) and also a bit more than usual on Friday (after work, maybe in preparation for the weekend) and Mondays (maybe to refill after a weekend).



# Recurring trends in specific categories


![png](Story_PartRadek_files/Story_PartRadek_52_0.png)



* One can observe that TRAVEL has cyclical spikes in months 6-8 (which coincides with summer) likely due to people going on vacation.

* At the same time there is a light drop in SPIRITS and PRODUCE sales which is likely explained by people going on vacation don't do their regular shopping or do it elsewhere (possibly abroad).

# Sales at different times of day


![png](Story_PartRadek_files/Story_PartRadek_56_0.png)


<span style="color: red">In final version add interactive charts where one can look at times of individual groups</span>


![png](Story_PartRadek_files/Story_PartRadek_62_0.png)



* Here we can see that older people tend to do the shopping in the late morning and early afternoon - starting at 9, and with a peak activity at 15.

* Adults tend to do most of their shopping later - with most of them shopping around 17-18.

* The youngest age group (19-24) tend to do the shopping in the evening - peaking around 18 and being relatively more active in the night.



![png](Story_PartRadek_files/Story_PartRadek_64_0.png)


As we can see the salad bar has a big spike at around 1pm which suggests lots of clients buy salads for lunch, the later increase around 5pm is likely caused by clients buying salads after work or during their normal shopping (overall sales also peak at ~5pm) for example for the next day.
