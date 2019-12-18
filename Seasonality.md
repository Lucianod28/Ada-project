---
layout: page
title: Seasonality
---

## Spending on days of week


We have analyzed how many transactions are made on each day.

Unfortunately, our data did not have labels specifying which number corresponds to which day of the week, so we made some assumptions.


![svg](Seasonality_files/Seasonality_7_0.svg)


As we can see, there are most transactions on days 6 and 7 and least on 2, 3 and 4.

We hypothesize that 6 and 7 are Saturday and Sunday because it is likely that more transactions would be made during the weekend as most people have time on these days to go shopping. One thing we have considered is that in many countries, shops are actually closed on Sundays, so that would result in a big drop of sales on that day, but there is no day that would be a clear outlier of having almost no transactions, so we assume that these shops operate on every day of the week.

The small increase on days 1 and 5 seems in line with this hypothesis, as people are likely going shopping slightly more often on Mondays, for example to refill after having guests on the weekend, and on Fridays for numerous reasons (to prepare for a weekend trip or a party, or just having finished work).

In addition, after looking at how many transactions people from each group are making, we can see that while most people's habits do not differ that much with age, there is is a tendency for older people to do shopping on Sundays much less often then younger ones.

The youth actually seem to prefer Sundays for shopping, while the seniors actually prefer Fridays.


![svg](Seasonality_files/Seasonality_16_0.svg)



![svg](Seasonality_files/Seasonality_17_0.svg)


## Sales at different times of day

We now check if there are any rush hours in the shops.


![svg](Seasonality_files/Seasonality_21_0.svg)


We now compare the amount of transactions on the weekends and the weekdays.


![svg](Seasonality_files/Seasonality_23_0.svg)


As the weekend lasts only 2 days and there are 5 weekdays, to get a fair comparison, we have divided the transaction amounts on weekends by 2 and by 5 on weekdays. So the bar height represents the average amount of transactions on one day of the respective period.

We can see that on weekdays there are much fewer sales between 9 and 16. This makes sense as during the week, most people work during that time. There are more sales in the early morning and late evening likely caused by people doing the shopping before or after work.

We now wanted to see how the usual transaction time varies by demographic.


![svg](Seasonality_files/Seasonality_28_0.svg)


Here we see that older people tend to do their shopping in the late morning and early afternoon - starting at 9, and with a peak activity at 15.

Adults tend to do most of their shopping later - with most of them shopping around 17-18.

The youngest age group (19-24) tends to shop in the evening - peaking around 18 and being relatively more active in the night.


![svg](Seasonality_files/Seasonality_30_0.svg)


As we can see the salad bar has a big spike at around 13, which suggests lots of clients buy salads for lunch; the later increase around 17 is likely caused by clients buying salads after work or during their normal shopping (overall sales also peak around 17).

## Long term correlations

We wondered if sales of some products correlate with others. We plotted sales in different categories and normalized them to see the correlations more easily.

(Some categories have very little sales over all, so even if they correlate with others it would be hard to see that on a plot without normalizing).


![svg](Seasonality_files/Seasonality_35_0.svg)


We can see that TRAVEL has cyclical spikes in months 6-8 (which coincides with summer), likely due to people going on vacation.

At the same time there is a light drop in SPIRITS and PRODUCE sales (PRODUCE is mostly daily food products). This can likely be explained by the fact that people going on vacation often don't do the regular shopping (for example because they are more likely to dine in a restaurant rather than cook) and go abroad (so their shopping is not counted in the dataset we have).
