# Symfony, Easy Peasy Lemon Squeezy 👩‍🎓

## Install dependencies

> Use composer to install dependencies in *vendor/* (needed libraries).  
  Install dependencies from `composer.lock` if exist or create it.


```bash
composer install
```

*If you encounter a bug, you need to do a composer update instead because I probably have a dependency for PHP 7.2 only so you need to fix it!*

```bash
composer update
```

> If you want to require a new dependency

```bash
composer require johndoe/library
```

## Configure Project

Configure file `.env` accordingly to **your** environment.

## Symfony Console

* Get all available commands

> Windows

```bash
php bin\console
```

> Mac

```bash
bin/console
```

* Start a Web Server

> Windows (foreground process)

```bash
php bin\console server:run
```

> Mac (background process)

```bash
bin/console server:start
```

* Create database (if not exist)

> Windows

```bash
php bin\console doctrine:database:create
```

> Mac

```bash
bin/console doctrine:database:create
```

* Update schema (execute SQL statements to sync tables/columns)

> Windows

```bash
php bin\console doctrine:schema:update --dump-sql --force
```

> Mac

```bash
bin/console doctrine:schema:update --dump-sql --force
```

## TODO

### Project

**Final date:** Sunday, January 27, 2018.

**Send method:** 
* GitHub (if you know how to use it) and email me the repository link.
* Email me the project via wetransfer directly.

**Email address:** thibaud.bardin+iim[at]gmail.com

Ps: *Do not send me the `vendor/` directory (or -1pt on the final grade)*

### General

Create a tiny shopping website with a front and an admin part (no real selling involved, no cart, ...).  
You definitely have the right to use the [EasyAdminBundle](https://symfony.com/doc/current/bundles/EasyAdminBundle/index.html)  

> And yes, you'll have to update the `Product` entity.  

**Minimum pages:**

├── /  
├── /product/{slug-of-the-product OR id-of-the-product}  
├── /login  
├── /logout  
└── /admin  

### Pages

> All pages must have a valid navbar to navigate to all available pages (with context, when not logged, don't display admin pages in navbar).  
  Plus the username OR email of the logged in user must be present in the navbar instead of "Login".

#### Pages > Homepage, path="/"

Show all products with a pagination (between 6-12 articles per page).  

Per product display the title, a description, the creation date (and the brand of the product).

#### Pages > Product path="/product/{slug}" OR path="/product/{id}" 

Show one product via its id OR [slug](https://github.com/cocur/slugify) with [Slugify Integration with Symfony](https://github.com/cocur/slugify#symfony).    

The page must display the name, the description, the creation date (and the brand of the product).  

*An image would be much appreciated but need a lot more work (so keep it in mind as a bonus point).*  

> https://symfony.com/doc/current/routing.html  

#### Pages > Login path="/login"

Shows a valid login form (username OR email + password).

#### Pages > Logout path="/logout"

Log out a user and redirect him to the homepage.

#### Pages > Admin

Protect this section to only logged in users (lucky you are, already done the code is).  
I want to be able to manage entities ([CRUD](https://en.wikipedia.org/wiki/Create,_read,_update_and_delete) mandatory):
- users
- products
- brands (optional, replace the text column of `Product`)

> If you want to try to have a Brand entity, read that before [Doctrine Association in Symfony](https://symfony.com/doc/current/doctrine/associations.html).  

### Design

The following is greatly appreciated:

* [Bootstrap 4](http://getbootstrap.com/docs/4.0/getting-started/introduction/) for design.
* [FontAwesome](http://fontawesome.io/get-started/) for icons.

Ps: *Don't forget*

### Requirements

You must at least use (and properly configure) the following tools/libraries:

* [Symfony](http://symfony.com/) 😍
* [Laravel](https://medium.com/@mantasd/guide-to-writing-bad-laravel-code-6c082bb0c68a) and it's °ZERO° 😱

### Good luck ✌️

![Good Luck](http://heyjackass.com/wp-content/uploads/2016/05/lando_goodbye.jpg)

## Shortcuts Jetbrains (bonus4free)

* Quick open `CMD + MAJ + O` (mac) | `CTRL + N` (windows)
* Reformat code `CMD + ALT + L` (mac) | `CTRL + ALT + L` (windows)
