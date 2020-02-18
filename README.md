# CodeIgniter 4 "Dev" Application Starter

NOTE: This repo is deprecated as of the official 4.0.0 release. It was originally made available for pre-release work
so is no longer necessary. If you require a similar setup, install the appstarter repo instead, and manually change
`composer.json` to point to the `dev-develop` branch.

## What is CodeIgniter?

CodeIgniter is a PHP full-stack web framework that is light, fast, flexible, and secure. 
More information can be found at the [official site](http://codeigniter.com).

This repository holds a composer-installable app starter.
It has been built from the 
[development repository](https://github.com/codeigniter4/CodeIgniter4).

**This is pre-release code and should not be used in production sites.**

--- 
 
**CAUTION: This app starter is EXPERIMENTAL, and likely to change before
the framework release. We are looking for feedback and suggestions!**  

---

More information about the plans for version 4 can be found in [the announcement](http://forum.codeigniter.com/thread-62615.html) on the forums.

The user guide corresponding to this version of the framework can be found
[here](https://codeigniter4.github.io/CodeIgniter4/). 

##Installation & updates

`composer create-project codeigniter4/devstarter -s dev` then `composer update` whenever
you want to pull the latest updates.

**Compare your `app/Config` folder to that inside `vendor/codeigniter4/codeigniter4/app/Config`,
as there could be changes in the latter that need to be copied
into yours.**

##Setup

Copy `env` to `.env` and tailor for your app, specifically the baseURL
and any database settings.

## Important Change with index.php

`index.php` is no longer in the root of the project! It has been moved inside the *public* folder,
for better security and separation of components.

This means that you should configure your web server to "point" to your project's *public* folder, and
not to the project root. A better practice would be to configure a virtual host to point there. A poor practice would be to point your web server to the project root and expect to enter *public/...*, as the rest of your logic and the
framework are exposed.

**Please** read the user guide for a better explanation of how CI4 works!
The user guide updating and deployment is a bit awkward at the moment, but we are working on it!

## Server Requirements
PHP version 7.2 or higher is required, with the following extensions installed: 

- [intl](http://php.net/manual/en/intl.requirements.php)
- [libcurl](http://php.net/manual/en/curl.requirements.php) if you plan to use the HTTP\CURLRequest library

Additionally, make sure that the following extensions are enabled in your PHP:

- json (enabled by default - don't turn it off)
- [mbstring](http://php.net/manual/en/mbstring.installation.php)
- [mysqlnd](http://php.net/manual/en/mysqlnd.install.php)
- xml (enabled by default - don't turn it off)
