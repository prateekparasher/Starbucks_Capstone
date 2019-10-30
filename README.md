## Starbuck's Capstone Challenge
Instructions for the project can be found in the Starbucks Project Workspace.

## Dataset overview
The program used to create the data simulates how people make purchasing decisions and how those decisions are influenced by promotional offers.
Each person in the simulation has some hidden traits that influence their purchasing patterns and are associated with their observable traits. People produce various events, including receiving offers, opening offers, and making purchases.
As a simplification, there are no explicit products to track. Only the amounts of each transaction or offer are recorded.
There are three types of offers that can be sent: buy-one-get-one (BOGO), discount, and informational. In a BOGO offer, a user needs to spend a certain amount to get a reward equal to that threshold amount. In a discount, a user gains a reward equal to a fraction of the amount spent. In an informational offer, there is no reward, but neither is there a requisite amount that the user is expected to spend. Offers can be delivered via multiple channels.
The basic task is to use the data to identify which groups of people are most responsive to each type of offer, and how best to present each type of offer.

### Motivation
This project to complete udacity Data Scientist Nanodegree capstone project  The dataset from the program that creates the data simulates how people make purchasing decisions and how those decisions are influenced by promotional offers. We want to make a recommendation engine that recommends Starbucks which offer should be sent to a particular customer.

### File Descriptions
The notebook available here showcases work related to the above questions.

This data set is a simplified version of the real Starbucks app because the underlying simulator only has one product whereas Starbucks actually sells dozens of products.

The data is contained in three files:

portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)
profile.json - demographic data for each customer
transcript.json - records for transactions, offers received, offers viewed, and offers completed
Here is the schema and explanation of each variable in the files:

### portfolio.json

id (string) - offer id
offer_type (string) - the type of offer ie BOGO, discount, informational
difficulty (int) - the minimum required to spend to complete an offer
reward (int) - the reward is given for completing an offer
duration (int) - time for the offer to be open, in days
channels (list of strings)

### profile.json

age (int) - age of the customer
became_member_on (int) - the date when customer created an app account
gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
id (str) - customer id
income (float) - customer's income

### transcript.json

event (str) - record description (ie transaction, offer received, offer viewed, etc.)
person (str) - customer id
time (int) - time in hours since the start of the test. The data begins at time t=0
value - (dict of strings) - either an offer id or transaction amount depending on the record

## conclusion

models here was adaboost by 65% for discount offer for bogo training I think company should focus to give more interesting offers to males since their income is higher and majority customers are between 50 to 60 year old, Discount and BOGO increase the customer buy rating
