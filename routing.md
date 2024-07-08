# Routing

Flint Framework utilizes Symfony/Routing, enabling powerful and flexible route management. Adding routes is simplified to a single line:

```php
addRoute('home', '/', 'App\Controllers\HomeController', 'index');

Routes with parameters are supported effortlessly: