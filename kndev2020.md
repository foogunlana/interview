# Stears Coding Homework

Thanks for your application to Stears

This interview is intended for a developer with experience in MongoDB, ReactJS, Typescript, NodeJS & NestJS.
So we expect that you use those tools to achieve the goal, or demonstrate a level of knowledge (or learning) of them.

We do not require that you complete this task, but that you attempt as much as you can so we will have enough information to assess your skill level.

#### Submissions

- Create a private [gitlab](https://gitlab.com/) repository and add foluso_ogunlana as a contributor
- Create a README.md with clear set up instructions (assume no knowledge of the submission or the stack)

#### Deadlines

You will be given 4 days to complete the tasks below before a video call interview.

#### Assessment

You will be assessed primarily on the following, **in this order**:

1. **Testing** - Prove proficiency in thorough automated testing to avoid regression
2. **User Experience** - Demonstrate good intuition and careful planning of your UI & UX
3. **Expertise** - Demonstrate knowledge of good practices & architecture in the NodeJS, Typescript, NestJS, MongoDB and React ecosystems
4. **Deployment** - Create code that can be shipped & iterated easily
5. **Documentation** - Provide documentation to get others up to speed on your work

Also we will give extra points for:

- **Flair** - Surprise us

#### Conduct

By submitting, you assure us that you have not shared the test with anyone else and that all work submitted is your own. Though you are allowed to use whatever online or offline resources you see fit to learn skills for the tasks.

# **Coding Homework**

**Please complete Task 1 and Task 2 (which work together). Task 3 is a bonus**

## Task 1

This is a purely backend task to assess your API building ability

Build an API with the following interface:

| Method |      Endpoint       |      Request Payload      |
| :----: | :-----------------: | :-----------------------: |
|  POST  |     /companies      | [company](./company.json) |
|  GET   | /company/:companyId |             -             |
|  POST  |      /reports       |  [report](./report.json)  |
|  GET   |      /reports?      |             -             |

GET /reports lets you filter reports by type, company or year.
There is a **One To Many** relationship between the companies and reports, respectively.

You get to decide what the response body to each call should be, and what kind of request validation is necessary. Also note that the JSON files provided are only examples. You can modify the structure as you see fit, but don't stray too far out.

1. Take a look at the example JSON files. **Are there any problems with the example JSON payloads?**
2. If so, **correct your JSON files and use the corrected versions**
3. There are acceptance criteria below to guide your choices

#### Acceptance Criteria

- Be able to create a new company with POST /companies
- Be able to get a single company with /companies/:companyId
- Be able to create a new report with POST /reports
- Be able to get a list of all reports with GET /reports
- Be able to get a list of reports of type 'X' with GET /reports?type=X
- Be able to get a list of reports of company 'Y' with GET /reports?companyId=Y
- Be able to see swagger Open API documentation of all the above
- Be able to run with a single docker-compose up, and access the server on localhost:5000
- Be able to run unit tests with npm run test
- Be able to run integration tests with npm run test:integration

## Task 2

This is a task to test your Front-End architecture skills, knowledge of modern ReactJS & Typescript patterns, and understanding of good UI & UX

Create a ReactJS application that has 2 pages. 1 for browsing through companies and the other for drilling down into a specific company to see specific information. Here is a rough wireframe:

![Wireframes](./company-report.png?raw=true "Wireframes")

Here are 2 user stories to help with creating these pages.

#### User Story 1 - User can see list of companies

As a user I should be able to view a list of companies currently available in the database. Including the company name, description, address, email, and the number of company reports available.

**Acceptance Criteria**

- Be able to see company cards for at least 3 companies with the name in bold
- Be able to see the following company data in each card: description, address, email, and number of reports
- Be able to click a company card to take you to it’s company page (implemented in the next user story)

#### User Story 2 - User can see individual company and list of reports

As a user I should be able to see company details and a list of reports. The basic functionality is detailed in the acceptance criteria, but the finer details are up to you to choose how to present.

- Given I have clicked on a company on the home page
- When I land on the company page
- Then I am able to see the company card (same as on home page), and a list of reports underneath it

**Acceptance Criteria**

- Be able to see a company card
- Be able to see the header of the table "Company X reports for 2020"
- Be able to see a list of company reports (**Only for 2020**) in a table with columns: name, period, assignee, submitted
- Be able to sort by columns: submitted
- Be able to click a row to see the PDF report via URL (not yet implemented)

## [Bonus] Task 3

This task requires you to modify both the backend and frontend of your application.

Add a search bar to the home page that allows me to perform full text search on the companies and reports.

Searches should go to the backend with an endpoint /search?

The user experience is up to you to figure out, but here are some acceptance criteria to guide you:

**Acceptance Criteria**

- Be able to search for 'Company X budget report' and receive results including 'Company X' and 'Company X budget report' and 'Company X balance sheet' and 'Company Y budget report', but not 'Company Y balance sheet'

- Be able to search for 'budget report' and receive results including 'Company X budget report' and 'Company Y budget report', but not 'Company Y balance sheet' or 'Company X' or 'Company Y'

- Be able to search for 'Company X' and receive results including 'Company X' and 'Company X budget report' and 'Company X balance sheet' but not 'Company Y' or 'Company Y balance sheet'

**Note**

Company X and Y, and budget report and balance sheet are just examples, but the idea is that your search results should always show some relevance to what was searched for.

## Thanks!

If you made it this far, thanks for your time.
We look forward to reviewing your solid application with you!
