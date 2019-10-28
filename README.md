# Demographic trends in retail

# Abstract
We would like to explore buying habits in different demographic groups and how these are impacted by 
advertising campaigns. Specifically, we want to know how buying habits differ between different age, 
sex, and household size groups. We also wonder if these groups may respond differently to advertising 
campaigns.
We will use the Dunnhumby “The Complete Journey” dataset for this because it contains information 
about all grocery purchases from a number of households, including everything they bought in a store 
and their demographic information.


# Research questions

* How living status of a person (owner or renter) influences the buying habits?
* How advertising campaigns impact the different categories people?
* What is the relation between the shop popularity and the amount of coupons they provide?
* Do some demographic groups tend to be more regular/irregular in their shopping schedule?
* Are there trends over time in the amount of money spent on shopping 
(altogether or in specific categories)?

# Dataset

We plan to use the Dunnhumby dataset (“The Complete Journey”). We will have to check if there are 
missing values (but the data seems to be mostly clean and ready to use) and join multiple tables 
to be able to relate types of households, their transactions and types of bought products.
The size of the data is not too big to make it impossible to compute on our personal computers, 
as the most important files are rather small, with the biggest one being transactions (136MB). 
The causal data table is the biggest file of all, we would need to use it if we want to analyse 
the marketing impact, however it has a rather simple structure so after parsing it and pickling 
it’s likely to be smaller and manageable to use.

# A list of internal milestones up until project milestone 2

* Check for missing data and other anomalies
* Prepare helper functions to load and preprocess the dataset
* Analyse the data and try finding interesting demographic and product groups 
(for example: various food products are in different aisles we may want to merge them into broader categories)
* See if any interesting data is missing (like some demographics being underrepresented)

# Questions for TAa

* The Dunnhumby dataset has a license that requires their permission for publicly publishing 
results obtained by using their dataset. As far as we know, we need to create a public webpage 
for the project report, can we expect any help from the TAs on getting the permission? Or maybe 
is the permission granted by default to all course attendants?
* Can we use external libraries that do not come with Anaconda by default?
* If we decide to correlate our results with another dataset and we are not sure at the moment 
can we add that dataset later?
