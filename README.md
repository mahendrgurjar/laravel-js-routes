# Laravel JS routes

Command for use Laravel routes in JS Files
With this package you can use laravel routes with laravel mix js.

## Usage:

```shell
composer require codiant/laravel-js-routes
```

Execute artisan command

```shell
php artisan route:js
```

Add the resource to webpack.mix.js:

```js
mix.js("resources/js/routes.js", "public/js/routes.js");
```

Add app path  `MIX_APP_URL` in .env file

And js file in your footer links file.

```js
<script src="{{asset('public/js/routes.js')}}"></script>
```

Now have the `route` function. 
First parameter of route function is the route name (same as in laravel).
Second is an array of parameters or an object of parameters.
Third is if you want to use absolute paths, by default true.

## Example Uses
```js
In laravel route file.
Route::post('/user', /*......*/)->name('user');

In js file
route('user');

Use with parameters
Route::post('/user/{id}', /*......*/)->name('user');

In js file
route('user', [1]);
route('user', {1});

Use parameter with name
Route::post('/user/{user_id}/post/{post_id}', /*......*/)->name('user');

In js file
route('user', [1, 2]);
route('user', {1, 2});
route('user', {'user_id': 1, 'post_id': 2});

```


## Contributing

Pull requests and issues are welcome.
