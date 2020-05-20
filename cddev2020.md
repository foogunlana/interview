# Stears Coding Homework

Thanks for your application to Stears

This interview is intended for a developer with knowledge / experience in some of the following: Database modelling, System design & architecture, NodeJS & Typescript.

We expect that you use those tools to achieve the goal to demonstrate some level of knowledge (or learning) of them.

We encourage that you complete the test requirements for us to correctly guage your current skill level.

#### Submissions

- Create a private [gitlab](https://gitlab.com/) repository and add @foluso_ogunlana & @jaymykels69 as maintainers
- Create a README.md with clear set up instructions (assume no knowledge of the submission or the stack)

#### Deadlines

You will be given at least 5 days to complete the tasks below before a video call interview.

#### Assessment

You will be assessed primarily on the following, **in this order**:

1. **Problem solving** - Meet the requirements. Produce a system that solves the problem in the best way you know
2. **Architecture** - Create a simple, easy to maintain, modern system with clear foresight of future requirements
3. **Quality** - Demonstrate your solution's correctness with unit tests, a clear README.md or other documentation. Also, make it easy to deploy with docker-compose or other methods.

Also we will give extra points for:

- **Flair** - Surprise us with your programming expertise / problem domain knowledge / depth of understanding of the tools being used

#### Conduct

By submitting, you assure us that you have not shared the test with anyone else and that all work submitted is your own. Though you are allowed to use whatever online or offline resources you see fit to learn skills for the tasks.

# **Coding Homework**

## Single Task

This is a purely backend task to assess your programming architecture

Build an API with the following interface:

| Method |  Endpoint  |            Request Payload            |          Response Payload           |
| :----: | :--------: | :-----------------------------------: | :---------------------------------: |
|  POST  | /downloads | http://www.example.com/free-movie.mp4 | `{ staticId: xxxx-xxxx-xxxx-xxxx }` |
|  GET   | /downloads |                                       |  [example-downloads](./links.json)  |

The API is a download service.

It awaits requests from its users. Each request ends in a queued download job. Users can fetch the status of a download at any point by getting all downloads `GET /downloads`.

We are most interested in seeing how you deal with a non-blocking service triggered by the API. So if you wish, you can mock the download job out with a 10 second sleep instead of implementing it. Contact us if you find this confusing.

#### Hint

- Use a queue!

#### Acceptance Criteria

- Be able to create a new download with POST /downloads
- Be able to get all downloads and their correct statuses with GET /downloads
- Be able to receive a response as soon as a download job is created, without waiting for the download to complete
- Be able to retry failed jobs a fixed number of times set by an environment variable
- Be able to run unit or integration tests with npm run test

## Thanks!

If you made it this far, thanks for your time.
We look forward to reviewing your solid application with you!
