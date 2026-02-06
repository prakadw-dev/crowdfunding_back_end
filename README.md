# crowdfunding_back_end

# A repo contain my She Codes Crowdfunding project back end

manual steps input for goal - running external API
monetary goal

allow supporter to do monetary&/steps
type of goal differenciate object for goal
1 key value pair accepts number (would be steps/ 'currency' money)

if i got everything working from the class - then add the steps goal

create 1 table only for table - goal1 steps & money // when supporter pledge then can pick one, then have the reference on the table

API MAP - user story - from login then click this this this


# Concept/Name
UpFunding/Fundarun - A crowdfunding platform where people will raise money to donate to cancer fighters based on their steps goals and others can pledge to support them.

# Intended Audience/User Stories
People who need money to reach their goal and people who want to contribute to donate.

As a runner, I want to post my steps and funding goal, also share my profile
As a supporter, I want to see projects, pledge money to ones I like, and the see the progress
As a user, I want to log in so my pledges and projects are tracked

# Front End Pages/Functionality

- Home
    List all runners
    Click to view details
- Runners Details
    See full info and all pledges
    Make a pledge if logged in
- Create Fundraiser
    Form to create new fundraiser (login required)
- Login/Signup
    Create account or login

# API Spec
URL	HTTP Method	Purpose	Request Body	Success Response Code	Authentication/Authorisation
/fundraisers/	GET	Get all fundraisers	N/A	200	None
/fundraisers/	POST	Create fundraiser	Fundraiser object	201	Logged in
/fundraisers/1/	GET	Get one fundraiser (with pledges)	N/A	200	None
/pledges/	GET	Get all pledges	N/A	200	None
/pledges/	POST	Create pledge	Pledge object	201	Logged in

# DB Schema
Users → Fundraisers (one user owns many fundraisers) Users → Pledges (one user makes many pledges) Fundraisers → Pledges (one fundraiser has many pledges)