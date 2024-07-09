## Table of Contents

- [Home](index.md)
- [Installation](installation.md)
- [Controllers](controller.md)
- [Routing](routing.md)
- [Helpers](helpers.md)
- [Contribution](contribution.md)

---

# Controllers

In the Flint PHP framework, controllers manage application logic and interact with views or return JSON data when used for API purposes. Here’s an enhanced guide on using controllers effectively:


## Creating Controllers

Controllers are located in the `app/controllers` directory and can be structured according to your application's requirements. Here’s a basic example:

```sh
namespace App\Controllers;

class HomeController
{
    public function index($params = [])
    {
        view('home');
    }
}
```

---

## Passing Parameters

Controller methods can accept parameters, facilitating flexible data handling:

```sh
public function index($params = [123, 'imran', 'kashif'])
{
    // Controller logic using $params
    view('home');
}
```

---

## Returning Responses

Controllers can return different types of responses, such as strings:

```sh
public function index()
{
    return 'Office Home Page';
}

public function show($id)
{
    return 'Showing details for office ID: ' . $id;
}
```

---
This flexibility accommodates diverse application needs.

## Rendering Views

Views are typically stored in the views directory and can be rendered using the view function:

```sh
public function index()
{
    view('home');
}
```

---

## Pass Data

Optionally, pass data to views using an associative array:

```sh
public function index()
{
    $data = [
        'title' => 'Home Page',
        'params' => $params
    ];

    view('home', $data);
}
```

---
This dynamically populates views with data.

## Returning JSON Data

For API endpoints, you can return JSON data using the json method:

```sh
public function apiData()
{
    $data = [
        'id' => 1,
        'name' => 'Flint Framework',
        'version' => '1.0'
    ];

    json($data);
}
```

---
This method simplifies API response handling by converting arrays to JSON format.

## Conclusion

Flint controllers provide structured control over application logic, seamlessly integrating with views or facilitating API responses through JSON. Organize controllers in the app/controllers directory and utilize PHP features to build scalable web applications.

For advanced techniques and further integration options, refer to PHP documentation and Flint framework resources.

