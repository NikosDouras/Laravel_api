Finished the project (without the bonus tasks 13,14):     https://github.com/NikosDouras/Laravel_api

This is the postman collection link: 
https://blue-star-586314.postman.co/workspace/New-Team-Workspace~f87bc7d1-a662-4940-9823-c0c57ad79d6b/collection/29416353-7d308c1a-eb3e-4a22-a5da-a190bf9eae22?action=share&creator=29416353

And a google drive doc with directions for postman and using the app, and the problems I run into.

using postman: https://docs.google.com/document/d/1Ph2bmtC9nJCOnbr-n0agC_wzn5R5Ag2AsbjnxnDPQkM/edit?usp=sharing
using the app: https://docs.google.com/document/d/1gcQb5Uex88CRybqyqSHMy07ZeIERcxystCC2IfzDajA/edit?usp=sharing
problems: https://docs.google.com/document/d/1v7b-cPRYXJtRw6gu27rQFuPnqmUywnHmOviy1N857n0/edit?usp=sharing

Probably the person that will try to run the app will face some problems that I faced myself when trying to run the app. that's due to compatibility problems. I created the app in an environment with PHP 8.0.28, Composer 2.6.2, Laravel Framework 9.52.15, which is probably what's causing the issue. However maybe the person that will try to run the app will be able to overcome the problems and run it successfully.

---Using the app---

Steps for running the app_v4:
You should have: 
PHP 8.0.28
Composer 2.6.2
Laravel Framework 9.52.15
mysql (adjust the settings in the app\.env file, for now port is set to 3306), or any other DB, just make sure to change the settings.

Open bash inside app_v4

git clone https://github.com/NikosDouras/Laravel_api.git

Install Dependencies: composer install

php artisan migrate 

Optional
php artisan tinker 				 //optional Creating dummy data for the 
User::factory()->times(25)->create();		//optional tables. User emails are random 
Game::factory()->times(100)->create();	//optional but the password for every user     
                                                                       // is “password”.

php artisan serve
