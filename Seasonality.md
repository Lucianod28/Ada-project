---
layout: page
title: Seasonality
---

## Spending on days of week


We have analyzed how many transactions are made on each day.

Unfortunately, our data didn't have labels specifying which number corresponds to which day of the week, but we tried to make some hypotheses.


![svg](Seasonality_files/Seasonality_7_0.svg)


As we can see, there are most transactions on days 6 and 7 and least on 2, 3 and 4. 

We hypothesize that 6 and 7 are Saturday and Sunday because it is likely that more transactions would be made during the weekend as most people have time on these days to go shopping. One thing we have considered is that in many countries shops are actually closed on Sundays, so that would result in a big drop of sales on that day, but there is no day that would be a clear outlier of having almost none transactions, so we guess that these shops operate on every day of the week.

The small increase on days 1 and 5 seems in line with this hypothesis, as people are likely going shopping slightly more often on Mondays for example to refill after having guests on the weekend and on Fridays for numerous reasons (to prepare for a weekend trip or a party, or just having finished work).

Also after looking at how many transactions people from each group are making, we can see that while most people's habits don't differ that much with age, there is is a tendency for older people to do shopping on Sundays much less often then younger ones.

The youth actually seems to prefer Sundays as their favorite shopping day, while the seniors are actually prefering Fridays.


![svg](Seasonality_files/Seasonality_16_0.svg)



![svg](Seasonality_files/Seasonality_17_0.svg)


## Sales at different times of day

We now look if there are any rush hours in the shops.


![svg](Seasonality_files/Seasonality_21_0.svg)


We now compare the amount of transactions on the weekends and the weekdays.


![svg](Seasonality_files/Seasonality_23_0.svg)


As the weekend lasts only 2 days and there are 5 weekdays, to get a fair comparison, we have divided the transaction amounts on weekends by 2 and by 5 on weekdays. So the bar height represents the average amount of transactions on one day of the respective period.

We can see that on weekdays there are much less sales between 9 and 16. Of course this makes sense as during the week, most people are working during that time. There are more sales in the early morning and late evening likely caused by people doing the shopping before or after work.

We now wanted to see how the usual transaction time varies by demographic.


![svg](Seasonality_files/Seasonality_28_0.svg)


Here we can see that older people tend to do the shopping in the late morning and early afternoon - starting at 9, and with a peak activity at 15.

Adults tend to do most of their shopping later - with most of them shopping around 17-18.

The youngest age group (19-24) tend to do the shopping in the evening - peaking around 18 and being relatively more active in the night.



![svg](Seasonality_files/Seasonality_30_0.svg)


As we can see the salad bar has a big spike at around 1pm which suggests lots of clients buy salads for lunch, the later increase around 5pm is likely caused by clients buying salads after work or during their normal shopping (overall sales also peak at ~5pm) for example for the next day.

## Long term correlations

We wanted to see if sales of some products correlate with others. We have plotted sales in different categories and normalized them to see the correlations more easily.

(Some categories have very little sales over all, so even if they would correlate with other it would be hard to see that on a plot without normalizing).


![svg](Seasonality_files/Seasonality_35_0.svg)


We can see that TRAVEL has cyclical spikes in months 6-8 (which coincides with summer) likely due to people going on vacation.

At the same time there is a light drop in SPIRITS and PRODUCE sales (PRODUCE is mostly daily food products). This can likely be explained by the fact that people going on vacation often don't do the regular shopping (for example because they are more likely to dine in a restaurant rather than cook) and go abroad (so their shopping is not counted in the dataset we have).
