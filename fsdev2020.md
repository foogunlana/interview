# Stears Coding Homework

Thanks for your application to Stears for the role: Senior Full Stack Developer.

This interview is intended for an experienced Python Django & ReactJS developer.

It should take you roughly 2 days to complete.

#### Submissions

- Create a private [gitlab](https://gitlab.com/) repository and add foluso_ogunlana as a contributor
- Create a README.md with clear set up instructions (assume no knowledge of the submission or the stack)

#### Deadlines

You will be given at least 4 days to complete the tasks below before a phone interview in most cases.

#### Assessment

You will be assessed primarily on the following, **in this order**:

1. **Testing** - Prove proficiency in thorough automated testing to avoid regression
2. **User Experience** - Demonstrate good intuition and careful planning of your UI & UX
3. **Expertise** - Demonstrate knowledge of good practices & architecture in the Python, JavaScript, Django and React ecosystems
4. **Deployment** - Create code that can be shipped & iterated easily
5. **Documentation** - Provide documentation to get others up to speed on your work

Also we will give extra points for:

- **Flair** - Surprise us

###### NOTE

The aim of this assessment is **not** to complete the tasks, though completing the tasks is encouraged. The aim is to demonstrate your skills in good software creation, learning, and maintenance. We will favour well tested and planned incomplete tasks to completed spaghetti code.

#### Conduct

By submitting, you assure us that you have not shared the test with anyone else and that all work submitted is your own. Though you are allowed to use whatever online or offline resources you see fit to learn skills for the tasks.

# **Coding Homework**

Use Python Django & ReactJS. If you feel you'd rather use something else, please send an email to foluso_ogunlana@stearsng.com to find out if it's okay (it's probably not). Your README.md shoud contain clear instructions on how to build, deploy and maintain the application.

**Please complete Task 1 and Task 2. Task 3 is a bonus**

### Task 1

Django application to create posts. Below is an example post:

```json
{
  "id": 1,
  "userId": 1,
  "url": "/posts/1",
  "title": "Nigerian airlines returns",
  "body": "...",
  "created": "2019-02-02",
  "modified": "2019-02-02",
  "tags": ["Nigeria", "Nigerian airlines"]
}
```

- Your application should be a REST api with 1 endpoint: `/posts`.
- It should be deployable with `docker-compose up`
- It should have an integration test suite covering all endpoints
- It should use a shared runner on GitLab to run the integration and unit tests

**API Acceptance Criteria**

- Be able to list posts with GET /posts
- Be able to create a new post with POST /posts
- Be able to get a specific post with GET /posts/<id>
- Be able to search for posts with GET /posts?...
- Create a script `seed.py` to load the API with fake posts through the endpoints. Use any fake data. e.g. [JSONPlaceholder](https://jsonplaceholder.typicode.com/)

**Technical Acceptance Criteria**

- No less than 90% test coverage on api endpoints
- Provide a `.gitlab-ci.yml` to run the tests and build the container on the [pipeline](https://docs.gitlab.com/ee/ci/yaml/) using [shared runners](https://docs.gitlab.com/ee/ci/runners/)
- Be able to run tests, migrations & the dev server with a simple command - hint: `pipenv run` using [Pipenv](https://pipenv.readthedocs.io/en/latest/)

**Hints**

- Use [Django REST Framework](https://www.django-rest-framework.org/)
- Search GitLab's docs for example .gitlab-ci.yml configs

### Task 2

ReactJS application to search for posts

As a user, I should be able to land on the home page of your application, enter a search term, be navigated to a search results page and provided with snippets of matching posts.

**UX Acceptance Criteria**

- Be able to type into a search bar, and click search.
- Be shown a list of matching posts with text and author.
- Be able to go back to the search bar by clicking a button at the top of the page.
- Be able to see designs roughly matching the wireframes below.
- Be able to search for posts created in task 1

**Technical Acceptance Criteria**

- Use 2 separate routes: / for home page and /search for search results
- Achieve no less than 90% unit test coverage
- Provide a `.gitlab-ci.yml` to run the tests and build the container on the [pipeline](https://docs.gitlab.com/ee/ci/yaml/) using [shared runners](https://docs.gitlab.com/ee/ci/runners/)
- Be able to run tests, migrations & the dev server with a simple command - hint: `npm run ...`

![Example table](/../master/search.png?raw=true "Wireframes")

**Note**

- We expect that your code uses best practices in testing, linting, documentation and ReactJS & Django architecture
- Serve both back end and frontend applications using `nginx` or other
- Containerize each application using docker so it can be run using `docker-compose up`
- Write a `README.md` file on each repo explaining clearly how to set up **and deploy** the application in development (docker compose) to any environment (Digital Ocean, AWS, or any other server) so it can be seen over a regular browser and HTTP.

### BONUS Task 3

Any attempt at this task is welcome.

1. Hook up an elastic search container and find a way to keep it in sync with your django database, so that every post is instantly indexed as it is created and re-indexed when modified.

2. Expose the search endpoint of this container and all endpoints of the two others using an api-gateway pattern with any favourite tech, e.g. nginx.

3. Use elastic search from the frontend instead of query the django application directly.

4. Write a single E2E test that checks when an item is searched on the UI, results are returned.

## Thanks!

If you made it this far, thanks for your time.
We look forward to reviewing your solid application with you!
