## Table of Contents

- [Home](index.md)
- [Installation](installation.md)
- [Controllers](controller.md)
- [Routing](routing.md)
- [Helpers](helpers.md)
- [Contribution](contribution.md)

---

## Flint PHP Framework: Routing

Routing in Flint is a powerful mechanism for defining URL patterns and associating them with specific controller actions. This streamlined approach makes it easy to structure your application's URL handling.

### Adding Routes

Flint provides the `addRoute` function to effortlessly define routes. It takes four arguments:

* **Route Name (string):** A unique identifier for the route.
* **URI Pattern (string):** The URL path that triggers the route.
* **Controller Class (string):** The fully qualified name of the controller class that handles the request.
* **Method (string):** The specific method within the controller class that is invoked.

Here's an example demonstrating how to map the root URL (/) to the index method of the HomeController:

Use code with caution.
```sh
addRoute('home', '/', 'App\Controllers\HomeController', 'index');
```

---


Similarly, you can map the path `/office` to the index method of the OfficeController:
```sh
addRoute('office_home', '/office', 'App\Controllers\OfficeController', 'index');
```

---

### URI Parameters

Flint allows you to capture dynamic segments in URIs using curly braces {}. These segments act as parameters that are passed to the corresponding controller method.

For instance, the following route definition captures any value after `/office/` as the `id` parameter and passes it to the `show` method of the OfficeController:
```sh
addRoute('office_show', '/office/{id}', 'App\Controllers\OfficeController', 'show');
```

In this example, a request to `/office/123` would match the `office_show` route, and the `show` method would receive the value `123` as the `id` parameter.
---

### Advanced Features

Flint leverages the robust routing components from Symfony, providing a rich set of features that empower you to create intricate routing configurations:

* Route Parameters: Define constraints to restrict the types of values allowed for captured parameters.
* Route Groups: Organize routes into logical groups for better maintainability.
* Route Prefixes: Add prefixes to route paths for a more structured URL hierarchy.
* Route Names: Assign unique names to routes, enabling convenient referencing throughout your application.

These features grant you the flexibility to tailor your routing setup precisely to your application's requirements.

### Conclusion

Flint's routing system, built upon the foundation of Symfony's routing components, offers an intuitive and versatile approach to defining and managing URL routes within your Flint application. It caters to both basic routing scenarios and more advanced use cases that involve parameter constraints and route groups.

For an in-depth exploration of the Symfony Routing features supported by
Flint's routing system, built upon the foundation of Symfony's routing components, offers an intuitive and versatile approach to defining and managing URL routes within your Flint application. It caters to both basic routing scenarios and more advanced use cases that involve parameter constraints and route groups.

For an in-depth exploration of the Symfony Routing features supported 