# Slim Framework 3 Skeleton Application

Use this skeleton application to quickly setup and start working on a new Slim Framework 3 application. This application uses the latest Slim 3 with the [Pug-php template renderer](https://github.com/pug-php/pug). It also uses the Monolog logger.

This skeleton application was built for Composer. This makes setting up a new Slim Framework application quick and easy.

## Comparison between raw PHP and Pug template files:

Raw PHP template body *(10 lines, 259 chars)*:
```php
<body>
  <h1>Slim</h1>
  <div>a microframework for PHP</div>

  <?php if (isset($name)) : ?>
    <h2>Hello <?= htmlspecialchars($name); ?>!</h2>
  <?php else: ?>
    <p>Try <a href="http://www.slimframework.com">SlimFramework</a></p>
  <?php endif; ?>
</body>
```
Pug template body *(8 lines, 148 chars)*:
```pug
body
  h1 Slim
  div a microframework for PHP

  if name
    h2 Hello #{name}!
  else
    p Try #[a(href="https://slimframework.com") SlimFramework]
```

## Install the Application

Run this command from the directory in which you want to install your new Slim Framework application.

    php composer.phar create-project lhsazevedo/slim-pug-skeleton [my-app-name]

Replace `[my-app-name]` with the desired directory name for your new application. You'll want to:

* Point your virtual host document root to your new application's `public/` directory.
* Ensure `logs/` is web writeable.

To run the application in development, you can run these commands 

	cd [my-app-name]
	php composer.phar start

Run this command in the application directory to run the test suite

	php composer.phar test

That's it! Now go build something cool.
