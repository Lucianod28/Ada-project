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

* How shopping habits or transactions are influenced by the status of a person (e.g owner or renter)? Moreover, is there a correlation between family composition and shopping habits?
* How advertising campaigns impact different categories of people?
* How types of promotions and promotions in general impact sales?
* What is the relation between the popularity of a shop and the amount of coupons it provides?
* Do some demographic groups tend to be more regular/irregular in their shopping schedule?
* Are there any longterm shopping trends? 

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

* We will have the following internal mini milestones:
    - **Week1: 29.10.2019 - 03.11.2019** 
        - Check for missing data and other anomalies
    - **Week2: 04.11.2019 - 10.11.2019**
        - Prepare helper functions to load and preprocess the dataset
    - **Week3: 11.11.2019 - 17.11.2019**
        - Analyse the data and try finding interesting demographic and product groups (for example: various food products are in different aisles we may want to merge them into broader categories)
    - **Week4: 18.24.2019 - 24.11.2019**
        - See if any interesting data is missing (like some demographics being underrepresented)

# A list of internal milestones up until project milestone 3

* We plan to create a data story for the third milestone.
* As internal organisation, we proposed to have the following internal mini milestones:
     - **Week1: 25.11.2019 - 01.12.2019**
         - First Half: Gather any particular findings we might have and try to make a sinthesys of things we should include in the datastory
         - Second Half: Look over technologies that might help us implement a good looking page like html, javascript (and plotting libraries)
     - **Week2: 02.12.2019 - 08.12.2019**
         - First Half: Make an Idea about how we would want our data story look like and decide the topic
         - Second Half: Implement a first version where we arrange things and link libraries and decide about what technologies we use (this includes creating the HTML template, CSS files and other requirements for the web page)
	
     - **Week3: 09.12.2019 - 15.12.2019**
         - The actual implementation process of the data story

     - **Week4: 16.12.2019 - 19.12.2019**
         - Small design refinements

# Questions for TAs

* The Dunnhumby dataset has a license that requires their permission for publicly publishing 
results obtained by using their dataset. Additionaly (to the best of our knowledge), a public webpage needs to be created
for the project report. Can we expect any help from the TAs on getting the permission? Or is the permission granted by default to all course attendants?
* Can we use external libraries that do not come with Anaconda by default?
* If we decide on correlating our results with another dataset (not sure at the moment),
can we add that dataset later?
