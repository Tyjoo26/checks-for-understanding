## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?
Rails new Cats -T (optional: -d="postgresql" --skip-spring --skip-turbolinks)
2. What do Models generally inherit from in rails?
ApplicationRecord
3. What do Controllers generally inherit from in a rails project?
ApplicationController
4. How would I create a route if I wanted to see a specific horse in my routes fitle assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
Go to routes.rb and type resources :horses or :horse?
5. What rake task is useful when looking at routes, and what information does it give you?
bundle exec rake routes gives you the route helper, URI, and action#controller
6. What is an example of a route helper? When would you use them?
company_job_path(argument) is a route helper example and is used in the controller. I'd use a route helper to make your redirects more flexible instead of hardcoding it.
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
path is a route helper,  url returns the entire url
8. What are strong params and why are the necessary?
Strong params is a hash that has key value pairs of inputs for forms. They are necessary for security, as you would want to keep strong params in a private method so there can be no outside manipulation of the values in a params hash.
9. What role does `form_for` play in helping us create our forms?
Form for is a form action that generates a form. It assigns the instance variable that contains an instance of a resources taht we will then populate the attributes with with the values passed in the form
10. How does `form_for` know where to submit the user's input?
Form for knows where to submit the users input by the instance variables beign passed in the top of the form for.
11. Create a form using a `form_for` helper to create a new `Horse`.
<%= form_for (@horse) do |f| %>
12. Why do we want to validate our models?
Our models need validation to ensure that data is being passed in an acceptable manner. For example, when we validate the presence of a form field, our model will not accept empty data fields when submitting infromation to the database.
