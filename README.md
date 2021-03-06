# Laravel 8 

## PHP help stop injection
- Strip_Tags($phpVariable);

## Composer install
### Check version 
- `composer --version`

## npm/node.js
### Check version
- `npm --version`
- `node --version`

## PHP
### Check Version
- `php -v`

## Tools Needed

- Visual Studio Code (VSCode) or PHPStorm as IDE
- Laragon or XAMPP for MySQL, PHP, and Apache
- Composer for PHP package installs
- Git for version control

## Prerequisites 

- At least PHP 7.3+ is required
- Bootstrap 5 for HTML components and styling
- Laravel CLI (`composer global require laravel/installer`)

## Setup List

### Create a New Project

1. `composer global require laravel/installer` (Install the Laravel CLI)
2. `laravel new example-app-name` (Create new project called **example-app-main**)
3. `composer create-project laravel/laravel example3 8.* --prefer-dist` - Version 8 (extra)
4. `cd example-app-name` (Navigate to **example-app-main** folder)

### Add **make:view** to Artisan Commands

1. `composer require theanik/laravel-more-command --dev`

### Add **Bootstrap CSS** to the build
1. `composer require laravel/ui` (laravel/ui is deprecated and they are using breeze or jetstream)
2. `php artisan ui bootstrap` (add `--auth` to auto-create authentication-related pages like login and register)
3. `npm install bootstrap@latest @popperjs/core --save-dev` (installs the latest version of Bootstrap and PopperJS)

### Steps to Continue installing
1. `npm install` (had an issue where mix was not installed until you do this.)
2. `npm run dev`
3. `npm run dev` (sometimes you have to run the this twice for **scss** to run again)
4. delete the Web Config file in the public folder if it is IIS. ??

## Laravel Tools (not sure if this is needed or not.  It was kinda cool looking providing good debug info.)
1. Laravel Debug Bar 
 `composer require barryvdh/laravel-debugbar --dev`

## Laravel Training

- [Laravel 8 from Scratch - Laracasts](https://laracasts.com/series/laravel-8-from-scratch/)
- [Eloquent or Query Builder: When to Use Which?](https://www.youtube.com/watch?v=uVsY_OXRq5o)

## Bootstrap Tricks

- [Use other colors in Bootstrap](https://www.youtube.com/watch?v=CTmubyW4uYo&t=1s)
- [Bootstrap 5 Installation on Laravel along with Utility API Example](https://www.youtube.com/watch?v=Zswg6_lISdU)

## Display Errors

```php
 if (! file_exists($path)) {
      dd('file does not exist!');
      ddd('file does not exist!'); // Prettier Error Message.
 }
```

## Add-ons

`composer require spatie/yaml-front-matter` // install YAML

## Command Line - Tinker (Create 3 Users)

```
php artisan tinker

$user = new App\Models\User;
$user->name = 'Jim Sample';
$user->email = 'jsample@gmail.com';
$user->password = bcrypt('!password');
$user->save();

$user = new App\Models\User;
$user->name = 'Stacey';
$user->email = 'Stacey@gmail.com';
$user->password = bcrypt('!password');
$user->save();`

$user = new App\Models\User;
$user->name = 'Nathan Stanford';
$user->email = 'Nathan.Stanford@gmail.com';
$user->password = bcrypt('!password');
$user->save();

User::all();  // List All Users

php artisan help make:migration // To get help information
```

## Create a migration table

`php artisan make:migration create_posts_table;`

## Add a new post to Post table

```php
$post = new App\Models\Post;
$post->title = 'Eloquent is Amazing';
$post->excerpt = 'Lorem ipsum dolar sit amet.';
$post->body = 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Unde rerum error laborum sed, velit commodi officia ea quo quia nihil nulla reprehenderit quas, corrupti consequuntur similique perferendis facilis vel odit doloribus eaque pariatur! Saepe quis reprehenderit dolores? Quis totam ipsam veritatis iure voluptas eos tempora eaque id, dolore accusamus impedit.';
$post->save();
```

## Other Tips

- You should **import the class first** before using it: `use App\Models\Post;`
- Be careful of **mass assign** and **mass update**.
- To exclude id field: `protected $guarded = ['id'];`
- To specify the fillable fields: `protected $fillable = ['title','excerpt','body'];`



## In routes/web.php page
- `Route::get('/posts', [PostController::class, 'index']);`

## And in View page
- `<a  href="{{url('/posts')}}">Posts</a>`

# Short List to create a brand new Laravel 8 app  
Always one less then the latest version since the modules are usually not ready for latest version.  Suggestion make sure NPM, Node, Composer, Chocolatey (windows) are up to date.
 
# laravel New App Steps (example app name "appname")
1. Create laravel version 8 App 
  c:\sites> composer create-project laravel/laravel appname 8.* --prefer-dist
  
2. Move into the new app root directory
  c:\sites> cd appname
  
3. optional add View to the "make:view" option
  c:\sites\appname> composer require theanik/laravel-more-command --dev
  
4. update project using npm (Can do npm i for npm install)
  c:\sites\appname> npm install 
  
5. Run npm Dev to setup development items (I run this twice)
  c:\sites\appname> npm run dev

