# Laravel 8 
# PHP 

## IDE Suggested
- Visual Studio Code - VSCode
- PHPStorm
- Laravel Breeze
- Bootstrap 5
- Tailwind CSS

## Prerequisites 
- Need PHP Installed 
- Need Composer installed
- To get Laravel CLI Installed - composer global require laravel/installer
- Need Laravel CLI
 

## Setup List
### Create a new project (either Step 1/2 or 3)
1. composer global require laravel/installer (install the Laravel CLI)
2. Laravel New  **example-app-name**
3. CD **example-app-name**

## Add make:view to the php artisan
1. composer require theanik/laravel-more-command --dev

## Add Bootstrap to the build
1. composer require laravel/ui
2. php artisan ui bootstrap (--auth)
3. npm install bootstrap@latest @popperjs/core --save-dev (installs the latest version of Bootstrap and PopperJS)
4. npm run dev
5. npm run dev
(sometimes have to run the npm run dev 2x after changes to scss run again.)  

## Bootstrap 
 
- [Use other colors in Bootstrap](https://www.youtube.com/watch?v=CTmubyW4uYo&t=1s)
- [Bootstrap 5 Installation on Laravel along with Utility API Example](https://www.youtube.com/watch?v=Zswg6_lISdU)
- [Eloquent or Query Builder: When to Use Which?](https://www.youtube.com/watch?v=uVsY_OXRq5o)

## Laravel Training
- [Laravel 8 from scratch - Laraacasts](https://laracasts.com/series/laravel-8-from-scratch/)

## Display Errors
```
 if (! file_exists($path)) {
      dd('file does not exist!');
      ddd('file does not exist!'); // Prettier Erro Message.
 }
```

## Add ons
- Insstall Yaml - composer require spatie/yaml-front-matter

## Commandline - Tinker (Create 3 Users)

- php artisan tinker

- $user = new App\Models\User;
- $user->name = 'Jim Sample';
- $user->email = 'jsample@gmail.com';
- $user->password = bcrypt('!password');
- $user->save();

- $user = new App\Models\User;
- $user->name = 'Stacey';
- $user->email = 'Stacey@gmail.com';
- $user->password = bcrypt('!password');
- $user->save();

- $user = new App\Models\User;
- $user->name = 'Nathan Stanford';
- $user->email = 'Nathan.Stanford@gmail.com';
- $user->password = bcrypt('!password');
- $user->save();

- List All Users
- User::all();

php artisan help  make:migration - to get help information.

## Create a migration table
- php artisan make:migration create_posts_table; 

## Add a new post to post table.
```
$post = new App\Models\Post;
$post->title = 'Eloquent is Amazing';
$post->excerpt = 'Lorem ipsum dolar sit amet.';
$post->body = 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Unde rerum error laborum sed, velit commodi officia ea quo quia nihil nulla reprehenderit quas, corrupti consequuntur similique perferendis facilis vel odit doloribus eaque pariatur! Saepe quis reprehenderit dolores? Quis totam ipsam veritatis iure voluptas eos tempora eaque id, dolore accusamus impedit.';
$post->save();
```
## You could setup before to use Class
- use App\Models\Post;

## Mass Assign be careful of this.
### Exclude ID
- protected $guarded = ['id'];
### Include 'title','excerpt','body'
- protected $fillable = ['title','excerpt','body'];

