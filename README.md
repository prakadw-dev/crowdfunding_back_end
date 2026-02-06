# crowdfunding_back_end

# A repo contain my She Codes Crowdfunding project back end

# Concept/Name

UpFunding/Fundarun - A crowdfunding platform where people will raise money to donate to cancer fighters based on their steps goals and others can pledge to support them.

# Intended Audience/User Stories

People who need money to reach their goal and people who want to contribute to donate.

As a runner, I want to post my steps and funding goal, also share my profile
As a supporter, I want to see projects, pledge money to ones I like, and the see the progress
As a user, I want to log in so my pledges and projects are tracked

# Front End Pages/Functionality

- Home
  - List all runners
  - Click to view details
- Runners Details
  - See full info and all pledges
  - Make a pledge if logged in
- Create Fundraiser
  - Form to create new fundraiser (login required)
- Login/Signup
  - Create account or login

# API Spec

| URL              | HTTP Method | Purpose                 | Request Body      | Success Response Code | Authentication/Authorisation    |
| ---------------- | ----------- | ----------------------- | ----------------- | --------------------- | ------------------------------- |
| /fundraisers/    | GET         | Return all fundraisers  | N/A               | 200                   | N/A                             |
| /fundraisers/    | POST        | Create a new fundraiser | Fundraiser object | 201                   | Must be logged in               |
| /fundraisers/:id | GET         | Return fundraiser by ID | N/A               | 200                   | N/A                             |
| /fundraisers/:id | PUT         | Update a fundraiser     | Fundraiser object | 20                    | Must be logged in and the owner |

# DB Schema

Users → Fundraisers (one user owns many fundraisers) Users → Pledges (one user makes many pledges) Fundraisers → Pledges (one fundraiser has many pledges)
