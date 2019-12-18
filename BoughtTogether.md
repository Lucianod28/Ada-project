---
layout: page
title: Products bought together
---

## Introduction

We wanted to explore relationships between different products - we decided to look for pairs of products that are bought together frequently.

First we look at counts of transactions that both products appear in.

The 5 most often occurring pairs are:

<small>(We converted the original product names like "TROPICAL FRUIT / BANANAS" to simple, slightly less specific names for simplicity. We also show rounded counts in thousands of transactions.)</small>

| Product 1    | Product 2    | Co-occurence count |
|--------------|--------------|--------------------|
| Bananas       | Milk         |  ~16k             |
| Milk         | Bread      |  ~14k             |
| Some soft drink (can) | Milk         |  ~11k             |
| Shredded cheese  | Milk         |  ~10k             |
| Refrigeated juice       | Milk      |  ~15k             |


As we can see, milk is present in almost every pair. This is likely because it is bought frequently overall.

Indeed, when we look at the top 5 most often bought products, we get almost the same results as for the top pairs:

| Product | Count |
|---------|-------|
| Milk    | ~66k   |
| Some soft drink (can) | ~39k |
| Other soft drink (2L bottle) | ~37k |
| Yogurt | ~37k |
| Bananas | ~30k |

Products that are bought more often are more likely to appear in the most frequent pairs (because if both products have high probability of being bought in a transaction, the join probability is also higher than for products that are bought rarely overall).

To explore further, we look at relative counts - for each pair we divide the co-occurrence count by the amount of transactions each of the products is in and take the bigger value.

## Relative count

Below we can see the top 5 pairs after relativizing the co-occurences. We also removed pairs which were bought less than 100 times (because when one product was bought only once ever, it would result in 100% but that is not a useful conclusion but rather an outlier).

The interpretation of percentage is: of all transactions where Primary product was bought, the fraction of transactions where Secondary product was bought as well.

| Primary product | Secondary product | % of times secondary product was bought along the primary one |
|-|-|-|
| Salad condiments (Salad bar) | Fresh fruit (Salad bar) | 91% |
| Fruit glazes | Strawberries | 73% |
| Instant breakfast | Milk | 73% |
| Frozen pizza (some particular variant) | Frozen meat entree | 72% |
| Salad dressing mix | Sour cream | 71% |

For example, we can see that 91% of the times Salad condiments were bought at the salad bar, fresh fruit was also bought. This correlation seems quite likely as these are 2 products from the salad bar, so they tend to be bought together quite often.

Then we can see that 73% of the time someone buys a fruit glaze, they also buy strawberries - of course they need something to put the glaze on, and strawberries look like a very common choice. Maybe it is a good idea for the retailers to do some promotions on buying these two together?

We can guess that the Instant breakfast is actually a kind of cereal package, as 73% of times it is bought it is bought with milk as well.

We can also see that people often buy sour cream along with the salad dressing. Also, many fans of frozen pizza also like an entree.

## Groups of products

The next goal was to look at groups of products bigger than mere pairs.

As there are exponentially many subsets of all products, we could not count them all, so we used an approximation. We look at pairs of products that are bought together often (after looking at the distribution of co-occurence counts, we decided for a threshold of sharing at least 1000 transactions) and form a graph. Then we look for cliques in this graph - a clique is a set of products in which each pair was often bought together.

We found that each pair formed from the following set of products has been bought together at least 3460 times:
 - Milk
 - Bananas
 - White bread
 - Shredded cheese
 - Potato chips
 - A soft drink in a can

In fact, there were 161 transactions that contained all of these items at once.

Again, it is not surprising to see milk and bananas in this list since they were bought very often. Thus, we again look at the relativized percentages. We looked at cliques in a similar graph but based on pairs where the relative percentage was at least 25%.

We found there are 32 transactions where all of:
- Milk
- Bananas
- Corn
- Green beans
- Green peas
- Carrots

were bought together. It is likely Milk and Bananas appear mostly due to their very high popularity, but the rest look like common ingredients for a homemade salad.

Moreover, we found 47 transactions where all of:
- Milk
- Tortilla / nacho chips
- Shredded cheese
- Mexican salsa
- Mexican beans (refried)
- Mexican seasoning mix

were bought.

Of course 32 and 47 are low numbers of transactions, but these contain the full set of all the listed ingredients. The amount of transactions in each subset is significantly greater.
