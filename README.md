# Pusher
Easy Laravel pusher integration with a function.

How this differs from other packages? Full auto-completion support with the Pusher PHP api.

Installation
`composer require kryptonit3/pusher:dev-master`

Set environment variables:

~~~
PUSHER_KEY=YOUR-PUSHER-KEY
PUSHER_SECRET=YOUR-PUSHER-SECRET
PUSHER_APP_ID=YOUR-PUSHER-APP-ID
~~~

Add the following to your Service Providers array (config\app.php)
```php
Kryptonit3\Pusher\PusherServiceProvider::class,
// for older PHP versions use 'Kryptonit3\Pusher\PusherServiceProvider',
```

Publish the config file. (not required unless you want to change some default settings)
~~~
php artisan vendor:publish
~~~
It will then be located in `config\kryptonit3_pusher.php`

you may now use all of the normal pusher calls with the `pusher()` helper function.

Example
```php
pusher()->trigger('my-channel-name', 'my-event-name', ['data' => true]);
```

Here are some more examples - https://github.com/pusher/pusher-http-php#publishingtriggering-events

Just replace the `$pusher->` with `pusher()->`
