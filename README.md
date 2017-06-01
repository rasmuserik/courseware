# Courseware

The purpose of this project is to make a simple tool for making online courses, - for people with wordpress blogs.

There is a big question about whether to use the existing wordpress backend, or add an additional backend. Both has benefits, but integrating with wordpress is choosen, as that means better integration(for logins/payment, etc.) and most importantly, that there will be no extra backend/service to maintain, even though it is not as nice to code.

Some notes / separate aspects of the project:

- [ ] Actual Course UI
  - [ ] Show course content
  - [ ] Course overview / menu
  - [ ] Keep track of progress
- [ ] Management of course content
  - [ ] Course content in CMS
  - [ ] Some encoding and storing of the course structure
- [ ] WordPress Generic Backend  (needed for storing user progress etc.)
  - [ ] Create wordpress plugin
  - [ ] User key-value store
    - [ ] Expose through wp-api
    - [ ] Create DB with
      - `user : userid`
      - `key : short string`
      - `value : binary`
      - `private: bool`
    - [ ] Add quota-support - limit amount of disk space user per user
- [ ] User authentication 
  - [ ] Use existing plugin?
  - [ ] User sign-up (with email)
- [ ] Payment / membership
  - [ ] Setup stripe payment
  - [ ] Sync stripe payments to user status
  - [ ] Use existing plugin?
- [ ] Access control?
  - [ ] Only show certain courses for members?
  - [ ] Dripping of content?
  - [ ] Use existing plugin?
- [ ] Deployment
  - [ ] test site to deploy too initially?
  - [ ] add user incremenally
    - [ ] A/B test membership conversion rate
