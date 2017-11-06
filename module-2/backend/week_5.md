1. How do we make flash messages display on a page?
  You would add a flash[:sucess] = "Flash message" in your controller which would render if certain logic is ran.
2. Where is cart information/temporary information usually stored?
  Cart information is temporarily stored
3. What might be some reasons not to store cart in our database? Are there any reasons why we would want to persist that information?
  If you have a cart displayed for visitors, and you allow visitors to add and remove things to a cart without having a user account, you wouldnt want to store your cart in the database. YOu'd want that information to persist and would most likely attach cart information to a session_id.
4. What is the purpose of the asset pipeline?
  The purpose of the asset pipeline is to make the parsing of data, stylesheets, and  images much more efficient and less time consuming. The asset pipeline achieves this by minifying files, precompiling files and concatening assets.
5. Why do we precompile our assets?
  We precompile our assets so they are read in one file. For example an application.css file would precompile all css files within the stylesheets folder so it is read once.
6. What do each of the following tags do?

```ruby
<%= stylesheet_link_tag "application" %>
<%= javascript_include_tag "application" %>
<%= image_tag "rails.png" %>
```
Tye Stylesheet link tag is parsed in an HTMl file and links to the application.main css file which precompiles all other css assets from one location. The javascript include tag evalutes and precomiples any javascript files that are linked in the application.css file. The image tag searches for the rails.png file within assets and references it.

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
A great Readme will include a brief synopsis of set up, including but not limited to: any associated gems, a link to documentation for each gem, testing gems, environment setup. It's better to spend up front time to develop a great Read me so future developers reading your read me don't waste hours trying to figure out how to start work on your project.

8. What are the top four accessibility issues that we as developers should be aware of? The top four accessibility issues are visual(ie: colorblindness), audio for individuals who are totally blind, language plugins for those who can't speak english, and cognitive.

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`? Before_save is an example of a callback, you typically don't want to use callbacks but if you had to use a before_save, the first place I'd like look to place it in is either a controller or model.

10. Given the following object, how would we create a scope for all users who are active?

```ruby
User.create(name: "Happy", active: true)
```
scope :active_user, -> (limit) { all(" desc").limit(limit) } ? Is this syntax right?

11. What is the difference between a scope and a class method?
My understanding is that a scope is a way of grabbing the right objects out youf database? A class method can do the same, but may be a bit more code intensive. A class method may also return a nil, but scopes, when chained together, will not return a nil.
