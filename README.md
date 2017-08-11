Iroute
=====

```PHP
Iroute::get('/', function() {
  echo 'Hello world!';
});

Iroute::dispatch();
```

Iroute also supports lambda URIs, such as:

```PHP
Iroute::get('/(:any)', function($slug) {
  echo 'The slug is: ' . $slug;
});

Iroute::dispatch();
```

You can also make requests for HTTP methods in Macaw, so you could also do:

```PHP
Iroute::get('/', function() {
  echo 'I <3 GET commands!';
});

Iroute::post('/', function() {
  echo 'I <3 POST commands!';
});

Iroute::dispatch();
```

Lastly, if there is no route defined for a certain location, you can make Iroute run a custom callback, like:

```PHP
Iroute::error(function() {
  echo '404 :: Not Found';
});
```

