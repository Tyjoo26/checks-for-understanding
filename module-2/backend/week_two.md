## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!).

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
  ActiveRecord is a Ruby DSL that provides an Object Relational Mapper to interact with SQL databases. It allows the user to map a database table to a Ruby object , and allows for full CRUD functionality.
2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
  Team.all gives you access to all the teams available that have been stored in the database.
  Team.new creates a new instance of team but doesnt save it
  Team.save saves a created instance of Team and stores it in the database
  Team.count counts the number of instances of team stored in database
  Team.create creates and saves a new instance of team into the database
  Team.find(id) grabs the first instance of team that matches the id

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team? Team.find(4) / Team.where(owner: Team.owner)

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
Team.owners.find(4)

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
Not sure about this one

6. Define foreign key, primary key, and schema.
A foreign key is a field in a table that identifes a row in another table. The row that the foreign key identifies is the primarh key of another table. A schema defines tables and indexes.
7. Describe the relationship between a foreign key on one table and a primary key on another table. A foreign key in one table is the primary key in another table
8. What are the parts of an HTTP response?
Response,
Status line / status code
optional body


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
  .where(argument) will search through your table for all instances of row in your table that matches the argument being passed in the params.
  .create will create and save an instance of a ruby object as a rown in your table
  .find will find the first instance of a ruby object that matches the argumetn being passed in your params

2. Name your three favorite ActiveRecord rake tasks and describe what they do.
3. What two columns does `t.timestamps null: false` create in our database?
:updated_at :created_at
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers? teachers :belongs_to school through: :classes
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)? Same as answer to Optional #4?
6. Give an example of when you might want to store information besides ids on a join table.
7. Describe and diagram the relationship between patients and doctors.
8. Describe and diagram the relationship between museums and original_paintings.
9. What could you see in your code that would make you think you might want to create a partial?
