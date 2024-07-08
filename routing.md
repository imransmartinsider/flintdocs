Routing
Routing in Flint framework allows you to define URL routes easily and efficiently. Flint utilizes Symfony Routing component, providing robust features for managing application routes.

Adding Routes
Adding routes is straightforward using the addRoute function. You can define routes in a single line with parameters specifying the route name, URI pattern, controller class, and method to invoke.

Basic Route
php
Copy code
addRoute('home', '/', 'App\Controllers\HomeController', 'index');
This example defines a route named home that maps to the root URI (/). It directs requests to the index method of HomeController.

URI with Path
php
Copy code
addRoute('office_home', '/office', 'App\Controllers\OfficeController', 'index');
Here, office_home route maps to /office, directing to the index method of OfficeController.

Route Parameters
php
Copy code
addRoute('office_show', '/office/{id}', 'App\Controllers\OfficeController', 'show');
The office_show route includes a parameter {id} in the URI pattern /office/{id}, directing to the show method of OfficeController. Parameters can be accessed within the controller method.

Advanced Features
Flint leverages Symfony's routing capabilities, enabling you to utilize advanced features such as:

Route Parameters: Define dynamic URI segments like /office/{id}.
Route Groups: Organize routes into logical groups for clarity and organization.
Route Middleware: Apply middleware to routes to handle cross-cutting concerns.
Route Naming: Assign unique names to routes for easy URL generation and linking.
Route Prefixes: Prefix routes to manage versions or subdomains effectively.
Additional Resources
For detailed information on Symfony Routing component and its advanced features, refer to the Symfony Routing Documentation.