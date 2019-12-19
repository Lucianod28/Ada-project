# Demographic trends in retail

# Abstract
We would like to explore buying habits in different demographic groups and how these are impacted by 
advertising campaigns. Specifically, we want to know how buying habits differ between different age, 
sex, and household size groups. We also wonder if these groups may respond differently to advertising 
campaigns.

We will use the Dunnhumby “The Complete Journey” dataset for this because it contains information 
about all grocery purchases from a number of households, including everything they bought in a store 
and their demographic information.

The project's site is hosted by Github using Github pages and can be foun here: https://lucianod28.github.io/Ada-project/

# Research questions

* What kinds of products are often bought together?
* What is the seasonality of various transactions? What are the rush hours?
* Are there any longterm trends in spending?
* How discounts impact sales? Who uses discounts most and what for?


# Dataset

We plan to use the Dunnhumby dataset (“The Complete Journey”). We will have to check if there are 
any missing values (but the data seems to be mostly clean and ready to use) and join multiple tables 
to be able to relate types of households, their transactions, and types of products bought.
The size of the data is not too big and can be handled on our personal computers. The most important files are rather small, with the biggest one being transactions (136MB). 

The causal data table is the biggest file of all, we would need to use it if we want to analyse 
the marketing impact, however it has a rather simple structure. Therefore, after parsing and pickling,
it’s likely to get smaller and become manageable to use.

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
* For the sake of internal organisation, we have the following internal mini milestones:
     - **Week1: 25.11.2019 - 01.12.2019**
         - First Half: Gather any particular findings we might have and try to make a sinthesys of things we should include in the datastory
         - Second Half: Look over technologies that might help us implement a good looking page like html, javascript (and plotting libraries)
     - **Week2: 02.12.2019 - 08.12.2019**
         - First Half: Get an Idea about how we would like our data story to look like and decide on the topic.
         - Second Half: Implement a first version where we arrange things, link libraries, and decide on what technologies to use (this includes creating the HTML template, CSS files and other requirements for the web page).
	
     - **Week3: 09.12.2019 - 15.12.2019**
         - The actual implementation of the data story.

     - **Week4: 16.12.2019 - 19.12.2019**
         - Small design refinements and last minute fixes.

# Questions for TAs

* The Dunnhumby dataset has a license that requires their permission for publicly publishing 
results obtained by using their dataset. Additionaly (to the best of our knowledge), a public webpage needs to be created
for the project report. Can we expect any help from the TAs on getting the permission? Or is the permission granted by default to all course attendants?
* Can we use external libraries that do not come with Anaconda by default?
* If we decide on correlating our results with another dataset (not sure at the moment),
can we add that dataset later?

# Contribution of team members

* Alexandru Placinta:
	- Set up deployment the Jekyll blog on Github pages + update the Jekyll theme
	- Dataset searches for anomalies
	- Research of the dataset for "Impact of advertising campaigns over different categories people" part of the datastory
* Luciano de la Igesia
	- Worked on the question of whether some demographic groups shop more frequently than others, unfortunately the answer was no so we didn't include this analysis on our website
	- Edited/revised all of the pages on the website
	- Wrote the home page of the website
* Radosław Waśko:
    - Some dataset preprocessing (adding DAYOFTHEWEEK, HOUR and MONTH columns)
    - Prepare datastory for Spending trends, Seasonality and Products bought together
    - Add Previous/Next buttons on the website, tweaked the sidebar
