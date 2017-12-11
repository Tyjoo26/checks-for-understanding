## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

1. List the five common HTTP verbs and what the purpose is of each verb.
  GET = Retrieves and reads a representation of a resource
  POST = Creates new resource
  PUTS = Updates entire resource
  DELETE = Destroys or deletes a specific resource and updates the index
  PATCH = Updates part of a resource

2. What is Sinatra?
  Sinatra is a domain specific language used with Ruby in order to create web based applications. In a nutshell, it's a series of pre-written methods that can be included in an application that can turn it into a ruby web app.

4. What is MVC?
  MVC stands for Models Views and Controllers. MVC is a representation of the flow of data from the client to the database. The Controller stores the routes and facilitates the client request and the route it needs to take to retrieve or modify that request. The Model contains the data and logic. And the views houses the code for visual representation.

5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
  We follow convention when creating our action/path names in order to make it easier for other developers to understand and maintain our code.

6. What types of variables are accessible in our view templates without explicitly passing them?
  Instance variables

7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?


  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?

```ruby
get '/horses' do
  name = "Mr. Ed"
  erb :index
end
```
9. What's the purpose of ERB?
  The purpose of ERB is to provide a layer to translate ruby into functional HTML.

10. Why do I need a development AND test database?
  You need to keep them separate so you can isolate and control your test cases for errors.

11. What is CRUD and why is it important?
  CRUD stands for Create Read Update Delete. It's important because it describes the functions for interacting with a database.

12. What does HTTP stand for?
  Hyper Text Transfer Protocol

13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?

  There are two ways to interpolate ruby. One is : <% %>. The second is : <%=  %>. The difference is the one with the equal sign will output the value or end result to the display while the other will not return the value to display.

14. What's an ORM?
  Object Relational Mapper

15. What's the most commonly used ORM in ruby (Sinatra & Rails)?
  ActiveRecord

16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
  1) get read index page
  2) get show index page
  3) get create new form
  4) get read edit form
  5) post submit form
  6) put/patch update resource by edit form
  7) delete destroys resource
  

17. What's a migration?
  Migration is the creation of a database table structure

18. When you create a migration, does it automatically modify your database?
  Nope, it creates the template for a table which is then populated with database data.

19. How does a model relate to a database?
  A model provides a reference to an object that represents a row of a table within our web app.

20. What is the difference between `#new` and `#create`?

  New creates an instance of an object but does not save it to the databse. Create does the creation and the saving to a database.

