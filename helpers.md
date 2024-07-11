## Table of Contents

- [Home](index.md)
- [Installation](installation.md)
- [Controllers](controller.md)
- [Routing](routing.md)
- [Helpers](helpers.md)
- [Contribution](contribution.md)

---

# Helpers

In the Flint PHP framework, helpers provide a convenient way to encapsulate and reuse custom functions and framework-related functionalities. Here's how you can effectively use helpers within your project:

## Custom Helpers

Custom helpers are stored in the helpers/custom directory and can contain functions tailored to your application's specific needs:

```sh
// helpers/custom/functions.php

function customFunction() {
    return "Hello from customFunction!";
}

function customFunctionNew() {
    return "Other Function!";
}

```

---
These functions can be called from anywhere within the framework without explicitly including them in each file.

## Custom Helpers Calling

Custom helpers can be used anywhere in whole application:

```sh
// Example usage in a controller method
public function index()
{
    return customFunction();
}


```

---
This simplifies code management and promotes reusability.

## Framework Helpers

Framework-related helpers are located in the helpers/framework directory. These functions provide additional functionalities specific to the framework. While you can modify or extend these functions, exercise caution as changes may affect core framework behavior:

```sh
// helpers/framework/functions.php

// Example of a framework-related function

function frameworkFunction() {
    return "Hello from frameworkFunction!";
}

```

---
Modify these functions only if you fully understand their implications on your project's functionality.

## Conclusion

Flint's helper system allows for encapsulating custom functions and accessing framework-related functionalities conveniently. By organizing custom and framework helpers in designated directories, you enhance code maintainability and facilitate efficient application development.

For more information on creating and utilizing helpers effectively, refer to PHP's documentation and additional resources specific to the Flint framework.


