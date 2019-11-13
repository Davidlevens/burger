<h1>Eat Da Burger</h1>

Live version: https://burger-beast.herokuapp.com/
<hr></hr>

Author: David Levens

Feel free to use some or all of this code if you're trying to complete a similar project.
<hr></hr>

<h3> App screenshot </h3>

![alt text](https://raw.githubusercontent.com/Davidlevens/burger/master/public/assets/img/demo.png "Burger App")

<h2> Project overview</h2>
Eat Da Burger is a full stack application utilizing MySQL, Node, Express, Handlebars and a homemade ORM. MVC design pattern implemented. Node and MySQL query and route data in the app, and Handlebars generates the HTML.

<hr></hr>

<h2> How it works </h2>
The user may enter any burger name to add it to the menu. This adds the new burger entry into the MySQL database. The initial burger entry is added as available on the menu and placed on the left side of the screen. The user may then eat any burger by clicking on it, which moves it into the adjacent column and updates its status accordingly in the database. They may delete the burger to clear it from the screen, too.
<hr></hr>

<h2>Technology used</h2>

[Node.js](https://nodejs.org/en/)

[Express](https://expressjs.com/)

[Heroku](https://heroku.com/)

[Handlebars](https://handlebarsjs.com/)

[MySQL](https://www.mysql.com/)

<hr></hr>

<h4>Below is a summary of how the app is structured and operates</h4>

- config
    - connection.js
        - establish database connection
    - orm.js
        - object for all of our SQL statement functions
            - all selects all burgers from database
            - create creates a new burger and inserts it into the database
            - update updates a database change
            - delete removes burger from database

- controllers
    - burger_controllers.js
        - routing for our burger app
            - get pulls all burgers from database and displays on screen
            - post and create will post new burger on screen and in database      
            - put and update will update database and move burger to devoured after button click
            - delete will remove burger from screen and database

    - db
        - schema.sql
        - seeds.sql
      
- models
    - burger.js
        - importing orm.js to create functions that will interact with database
    
    - public
        - assets for images, css and simple js file
        - app.get to pull survey page

- views
    - handlebars functionality

- server.js
    - configuration of server and application