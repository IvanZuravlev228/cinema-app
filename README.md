<h1 align=center><img src="https://cdn-icons-png.flaticon.com/512/3418/3418886.png" width=50>cinema-app<img src="https://cdn-icons-png.flaticon.com/512/3418/3418886.png" width=50></h1>
<p>A web application that simulates the operation of a ticket service in a movie theater. The application can register and authorize users and grant them different access rights depending on their credentials. The application can accept JSON objects and return a JSON response. When the program starts, two users are added to the database:</p>
<ul>
  <li><strong>ADMIN</strong>: username: <code>admin@i.ua</code>, password: <code>admin123</code></li>
  <li><strong>USER</strong>: username: <code>user@i.ua</code>, password: <code>user1234</code></li>
</ul>

<h2>Functionalities</h2>
<ul>
  <li>Add a new user</li>
  <li>Authorize the user</li>
  <li>Manage tickets</li>
  <li>Manage cinema halls</li>
  <li>Manage movie sessions</li>
  <li>Create a user's shopping cart</li>
</ul>

<h2>How to Run</h2>
<p><strong>WARNING</strong>. To start, you must have a servlet container(Tomcat) and a database(MySQL) installed on your computer</p>
<ul>
  <li>Clone the <a href="https://github.com/IvanZuravlev228/cinema-app.git">repo</a></li>
  <li>Open <a href="https://github.com/IvanZuravlev228/cinema-app/blob/main/src/main/resources/db.properties">db.properties</a> file and write information about your database</li>
  <li>Configure Apache Tomcat version 9.0.50 Artifact: war-exploded artifact, Application context: "/"</li>
  <li>For testing you can use query <a href="https://universal-flare-864500.postman.co/workspace/My-Workspace~ff3d5351-47dd-4913-8ca5-e613a73d0285/collection/27144104-8605f9d6-e1d1-40b2-bd53-e576f099cce8?action=share&creator=27144104">collection</a></li>
  <li>To get acquainted, you can watch the <a href="https://youtu.be/4wv7-XSG9oA">video presentation</a></li>
</ul>

<h2>Project has multiple endpoints with user and admin access</h2>
<ul>
  <li><code>POST: /register</code> (to create a user) - ALL</li>
  <li><code>POST: /cinema-halls</code> (to create a cinema hall) - ADMIN</li>
  <li><code>POST: /movies</code> (to create a movie) - ADMIN</li>
  <li><code>POST: /movie-sessions</code> (to create a movie sessions) - ADMIN</li>
  <li><code>POST: /orders/complete</code> (to create an order for current user) - USER</li>
  <li><code>PUT: /movie-sessions/{id}</code> (to update a movie session) - ADMIN</li>
  <li><code>GET: /orders</code> (to get order history for current user) - USER</li>
  <li><code>GET: /shopping-carts/by-user</code> (to get a shopping cart for current user) - USER</li>
  <li><code>GET: /cinema-halls</code> (to get all cinema halls) - USER or ADMIN</li>
  <li><code>GET: /movies</code> (to get all movies) - USER or ADMIN</li>
  <li><code>GET: /movie-sessions/available</code> (to get all available movie by date) - USER or ADMIN</li>
  <li><code>GET: /users/by-email</code> (to find user by email) - ADMIN</li>
  <li><code>PUT: /shopping-carts/movie-sessions</code> (to add movie session to shopping cart) - USER</li>
  <li><code>DELETE: /movie-sessions/{id}</code> (to delete a movie session) - ADMIN</li>
</ul>
<p>You can use Postman for testing</p>

<h2>Project Structure</h2>
<img src="https://github.com/IvanZuravlev228/cinema-app/blob/main/img_read_me/project_structure.png?raw=true">

<h2>Technologies</h2>
<ul>
  <li>Java v.17.0.5</li>
  <li>Maven v.3.8.7</li>
  <li>Spring(Core, Web MVC, Security) v.5.3.20</li>
  <li>Hibernate v.5.6.14.Final</li>
  <li>MySql v.8.0.22</li>
  <li>Java Servlets v.4.0.1</li>
  <li>Jackson core v.2.14.1</li>
  <li>Javax annotation v.1.3.2</li>
  <li>Tomcat v.9.0.50</li>
 </ul>
<h2>Contacts</h2>
<p>I will be happy to answer any questions and get to know each other better through <a href="https://www.linkedin.com/in/ivan-zhuravlev-199a12211/">LinkedIn</a></p>
