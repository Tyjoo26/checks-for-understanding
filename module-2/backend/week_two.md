## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!).

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
  ActiveRecord is an Object Relational Mapper. It provides a domain specific language that allows you to wrap rows of data into instance of Ruby Classes for manipulation and access.
2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?

  Some examples of methods you can call on "Team" are class methods. ActiveRecord has built in class methods that involves interacting with the database. For example: Task.all, Task.find(:id), Task.destroy, Task.save, Task.create

  We have access to these methods because we inherit from ActiveRecord base, where there are built in Ruby methods available.

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?

Team.find(4)
Team.find_by(owner: Owner_name)


4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
Owners.team.find(4)

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
Student belongs to Teacher, Teacher has many Students

6. Define foreign key, primary key, and schema.
A foreign key is a field in a table that identifies a row in another table. A foreign key is placed on the table that belongs to another table. So if a Director has many Movies, the Director ID Column would be the foreign key associating the two tables and would need to be added to the Movies table.  A schema defines tables and indexes.

A primary Key is the foreign key on another table. So Director ID is a primary  key that lives in the Director Table, but it is the foreign key that is added as a column to the Movie Table.

7. Describe the relationship between a foreign key on one table and a primary key on another table. A foreign key in one table is the primary key in another table

8. What are the parts of an HTTP response?
Response,
Status line / status code
Header
optional body


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
  .where(argument) will search through your table for all instances of row in your table that matches the argument being passed in the params.
  .create will create and save an instance of a ruby object as a rown in your table
  .find will find the first instance of a ruby object that matches the argumetn being passed in your params
  .save saves a newly created instance of a resource

2. Name your three favorite ActiveRecord rake tasks and describe what they do.
Rake db:migrate = migrates
rake db:create = creates database
rake db:drop = nuclear option
3. What two columns does `t.timestamps null: false` create in our database?
:updated_at :created_at
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers? teacher belongs to school, school has many teachers
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
6. Give an example of when you might want to store information besides ids on a join table.
You can create custom columns that do analysis of columns of tables that are being joined
7. Describe and diagram the relationship between patients and doctors.
Patients belong to doctors, doctors has many patients
8. Describe and diagram the relationship between museums and original_paintings.
9. What could you see in your code that would make you think you might want to create a partial?
A form that is used consistently through the CRUD of a resource.
