Interview for Web Developer June 18
===================================

Thanks for your application to Stears.
The interview will consist of 2 parts:

* [Coding homework](#coding-homework)
* [Technical questions](#technical-questions)

This interview is intended for a developer who is primarily skilled in front-end development, but has sufficient knowledge of back-end development tools.

#### Submissions
Please create a private [bitbucket](https://bitbucket.org/) repository and add foluso_ogunlana@stearsng.com as a contributor.

#### Deadlines
You will be given at least 2 days to complete the tasks below. You may also bring the task to your in-person interview to be completed there (you will be given time to do so).

#### Assessment
You will be assessed primarily on the following, in this order:
* **User Experience** - Keep the user in mind (device type, user flow, etc)
* **Maintainability** - Keep future programmers in mind (write tests, etc)
* **Portability** - Keep change in mind (changing requirements, servers, architectures, management, etc.)

Also we will give extra points to:
* **Security** - Keep secrets, passwords and databases safe
* **Architecture** - Use best practices in design and create simple readable code

###### NOTE
The aim of this assessment is **not** to complete the tasks, though completing the tasks is encouraged. The aim is to demonstrate your skills in good software an UX architecture, learning, and creating maintainable and portable code. We will favour well thought out incomplete tasks to completed tasks made with spaghetti code.

#### Conduct
By submitting, you assure us that you have not shared the test with anyone else and that all work submitted is your own. Though you are allowed to use whatever online or offline resources you see fit to learn skills for the tasks.

## **Coding Homework**

The coding homework is broken down into tasks to help you step through it in chunks. You must complete task 1, and either of task 2 or 3.
We advise you skim through all tasks before starting. Remember that completing all parts of a task is not as important as doing what you can in the best way you can.

#### **Platforms**
JavaScript, Python, PHP, Ruby and other scripting languages are preferred, but feel free to use anything that get's the job done. If you feel your tools are particularly obscure, please send an email to foluso_ogunlana@stearsng.com to find out if it's okay to use them.

**Please complete task 1 and either task 2, or task 3**

#### Task 1

Make a single page application similar to the Google home page. The only relevant feature here is the search bar. It should:
- Autocomplete results with a drop down
- Present a separate list of results beneath it when clicked
- Do nothing when a presented result is clicked
- Get results from records that will be entered in the same application

**On the same page**, create a form for entering articles which consist of a headline and a body. Any articles entered are saved to a database of your choice for searching via a REST api.
However, only the headlines should be considered when searching.

Finally, verify the behaviour of the app with automated unit tests.

#### Task 2

First, create a login page. The search page can only be accessed by logging in via email address and password. However, no need for a registration page.

Next, write a command line tool or command to add a new user to the user database. It should take an email address as an argument and then prompt the user to type in a password. After this, the user should be able to login freely.

Finally create a README.md or other documentation form explaining how to build, test, deploy or scale your application. It should also explain how to maintain the application - for instance what frameworks are used and how to test the API is working properly.

#### Task 3

First, containerise your application so it is easy to build, test, deploy and scale (if necessary) with few commands and in any host or environment.

Finally, add one more form to the application search page. One for commodities, in which the user could input a commodity name and a price in Naira to the database - e.g. "oil" and "50.3". Now your search bar should search for both the articles and the commodities, and it should present results in the same list in order of relevance.


## **Technical Questions**

Please keep your answers brief. Maximum of a couple of paragraphs.

- What part of your existing codebase needs the most improvement and how would you improve it if you had time.
- How would you divide the tasks above amongst multiple developers collaborating through Git? How many developers do you think would be necessary?
- What is your recommended process for updating the codebase with new requirements and features?
- How would you improve the UI UX instructions given in Task 1? Can you provide a rigorous process for gathering feature requests and turning them to requirements and acceptance tests?


## Thanks!

If you made it this far, thanks for your time.
We look forward to reading your code!
