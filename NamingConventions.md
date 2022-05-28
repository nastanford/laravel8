# Naming Conventions for Laravel

* Variables	=>	camelCase	=>	$articlesWithAuthor
* Collection Variable	=>	descriptive, plural	=>	$activeUsers = User::active()->get()
* Object Variable	=>	descriptive, singular	=>	$activeUser = User::active()->first()
* View	=>	snake_case	=>	show_filtered.blade.php
* Controllers	=>	singular, ProperCase	=>	ArticleController
* Model Name	=>	singular, ProperCase	=>	User, FollowingRequest
* Model attribute/property	=>	snake_case	=>	$model->created_at
* Method	=>	camelCase	=>	getAll
* Method in resource controller	=>	table	=>	store
* Method in test class	=>	camelCase	=>	testGuestCannotSeeArticle
* hasOne/belongsTo relation	=>	singular	=>	articleComment
* Other relations	=>	plural	=>	articleComments
* Table Name =>	plural	=>	article_comments
* Table column	=>	snake_case without model name	=>	meta_title
* Route	=>	plural	=>	articles/1
* Named route	=>	snake_case with dot notation	=>	users.show_active
* Primary key	=>	-	=>	id
* Foreign key	=>	singular model name with _id suffix	=>	article_id
* Pivot table	=>	singular model names in alphabetical order	=>	article_user
* Migration	=>	-	=>	2017_01_01_000000_create_articles_table
* Config and language files index	=>	snake_case	=>	articles_enabled
* Config	=>	snake_case	=>	google_calendar.php
* Contract (interface)	=>	adjective or noun	=>	Authenticatable
* Trait	=>	adjective	=>	Notifiable
