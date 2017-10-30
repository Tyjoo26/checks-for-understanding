## Week Four Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

* What is a cookie?
A cookie is data that's stored on a client. Cookies contain data about the client and interacts with a server when you access websites.
* What’s the difference between a session and a cookie?
A session is data stored on a server, and a cookie is stored on the clients computer?

* What’s a flash and when do you want to use flashes?

* Why do people say “HTTP is stateless”?
HTTP contains no data about the client. HTTP doesnt retain any information about a clients state when a client interacts with a browser using HTTP.
* What’s authentication? Explain.
Authentication is the principle behind client interaction with websites involving the use of user profiles. A visitor goes to a website, creates an account and stores user profile data. When that visitor logs in, they are authenticated by their user profile data and afforded certain rights.
* What’s the difference between authentication and authorization?
Authentication is the process of creating user profiles, authorization is the process of affording user profile types certain access rights.
* What’s a before filter?
A before filter is used in controllers to assign access priviledges to certain user profiles(for example: admin rights)
* How do we keep track of a user once they’ve logged in?
We keep track of a user by use of cookies.
* When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
You want to namespace a resource when assigning admin privileges. You'd want to nest resources when the creation of a nested resource is entirely dependent on the parent resource. For example, if a job belongs to a category and the creation of a job explicitly involves the identification of a category, youd want to next the job resource in a category resource block.
* At a high level, what tools can you use to implement authorization? How would you use them?
Enums is an example of an authorization tool. It's used to assign access roles to an array index for easy usage in testing.
* What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
An enum is an array used for user profile roles. It offers advantages in speed and its efficient use of processing power. Enums involve the assign of user access rights to an array index. You declare an enum in your models folder.
* What are some strategies you can use to keep your views DRY?
