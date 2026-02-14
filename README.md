# crowdfunding_back_end

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

| URL              | HTTP Method | Purpose                 | Request Body      | Success Response Code | Authentication/Authorisation        |
| ---------------- | ----------- | ----------------------- | ----------------- | --------------------- | ----------------------------------- |
| /fundraisers/    | GET         | Return all fundraisers  | N/A               | 200                   | N/A                                 |
| /fundraisers/    | POST        | Create a new fundraiser | Fundraiser object | 201                   | Must be logged in                   |
| /fundraisers/:id | GET         | Return fundraiser by ID | N/A               | 200                   | N/A                                 |
| /fundraisers/:id | PUT         | Update a fundraiser     | Fundraiser object | 200                   | Must be logged in and the owner     |
| /pledges/        | GET         | Return all pledges      | N/A               | 200                   | N/A                                 |
| /pledges/        | POST        | Create a new pledge     | Fundraiser object | 201                   | Must be logged in                   |
| /pledges/:id     | GET         | Return fundraiser by ID | N/A               | 200                   | N/A                                 |
| /pledges/:id     | DELETE      | Delete a pledge by ID   | N/A               | 204                   | Must be logged in and the supporter |
| /users/          | GET         | Return all users        | N/A               | 200                   | N/A                                 |

# DB Schema

Users → Fundraisers (one user owns many fundraisers) Users → Pledges (one user makes many pledges) Fundraisers → Pledges (one fundraiser has many pledges)

# Screenshots

- [ ] A link to the deployed project - https://crowdfunding-prod-app-3a60ea528749.herokuapp.com/
- [ ] A screenshot of Insomnia, demonstrating a successful GET method for any endpoint - https://ibb.co/x9zkMsM
- [ ] A screenshot of Insomnia, demonstrating a successful POST method for any endpoint - https://ibb.co/kVXvVrTf
- [ ] A screenshot of Insomnia, demonstrating a token being returned - https://ibb.co/Mkpv56Cd
- [ ] A screenshot of Insomnia, demonstrating a successful DELETE method for Pledge endpoint - https://ibb.co/5xc81ZdR
- [ ] Step by step instructions for how to register a new user and create a new fundraiser (i.e. endpoints and body data) - New user https://ibb.co/WNX4YcJB - New Fundraiser https://ibb.co/zV2kXzp7
      Using the endpoint https://crowdfunding-prod-app-3a60ea528749.herokuapp.com/fundraisers/ to create a new fundraiser, add Body JSON for title, description, goal, image, and "is_open"; make sure you're logged by adding the token through "Auth" tab.
      Using the endpoint https://crowdfunding-prod-app-3a60ea528749.herokuapp.com/pledges/ to create a new user, add Body JSON for id, owner, amount, comment, anonymous, fundraiser, and supporter; make sure you're logged by adding the token through "Auth" tab.
- [ ] Your refined API specification and Database Schema.
