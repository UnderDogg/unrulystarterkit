
# Demo

http://dev.unrulynatives.com

A DB-fed list of available features is available in
[DEMO app here](http://dev.unrulynatives.com/package)

# What it is
1. This is an instance of Laravel PHP Framework 5.3. A starter app. Its philosophy is slightly different than similar starter kits. Here are the highlights:

- all changes made over the original Laravel App have COMMENTS FOR BEGINNERS. You can delete them as soon as you consider them not necessary. 

- some solutions have variants, so that everyone one can pick the variant which suits their needs of the moment

- I have installed theme system (igaster/laravel-theme) to provide solutions for different CSS frameworks. You can switch between them at will:

3. I am an amateur programmer, not a pro. The repository is a self-teaching tutorial, in a sense. This app was originally my private repository of snippets, solutions, answers from StackOverflow and ideas to approach my needs. It aggregates all code which might come useful, and was appplied across many various projects.

### for the original Laravel Framework go to [Laravel Repository](https://github.com/laravel/laravel)




# FEATURES

A complete, DB fed list of implemented and future features is avalable at the [DEMO site](http://dev.unrulynatives.com). Most of the features are developed by preconfigured 3rd aprty packages.

## Assorted solutions

    - A gravatar displaying code (see model `getGravatarAttribute` in `App/User.php`).

    - slugs for models powered by `cviebrock/eloquent-sluggable` package.

    - Two themes pre-defined, powered by `igaster/laravel-theme`.

    - some examples of `intervention/image` for manipulating images.

    - login by invoking modal.

    - QR code generator for any page, reloads for changes of hashtag value (See JS feature above). Provided by `simplesoftwareio/simple-qrcode`

    - the app can recognize type of user's device, thanks to `jenssegers/agent`.

    - Date presenters provided by `jenssegers/date` package. Extra helpers also available

    - A simple upvoting system powered by `rtconner/laravel-likeable`.

    - Model tagging powered by `rtconner/laravel-tagging`.

    - commenting of models powered by `slynova/laravel-commentable`.





## Admin-oriented tools

    - Mass removal of records with field `status` == `null`. Easily adjustable for other purposes.

    - Wholesale recreation of slugs. Needed when you decide to implement slugs after a number of records is already submitted by users

    - user tracking (`spatie/laravel-activitylog`)


    - `/admin/server-status` - point your browser here to display server status, Laravel version and php version

    - DB and app backup powered by `spatie/laravel-backup`. A cron job pre-configured.

    - permission system provided by `spatie/laravel-permission`.

## Develpler-oriented tools and features

    - Laravel debugbar
    - A very handy scaffolding interface, DB-powered. `Amranidev/scaffold-interface`.
    - some scaffolding methods provided by `laralib/l5scaffold`.
    - manage translation files - URL `translations`. Powered by `barryvdh/laravel-translation-manager`.
    - see logs of your app thanks to `arcanedev/log-viewer` package.
    - 

## CSS/JS hacks and improvements over used frameworks:

    - Bootstrap: dropdown on hover  (see `css/common_elements.css`)
    - Bootstrap: button with icon on one side. See example at `docs/components_common`.

    - CSS classes for common CSS elements which I use most frequently. All are listed here `docs/components_common`


## JS & jQuery SCRIPTS

    - A script to load DOM patches via jQuery (`js/minitool_dom_patch.js`). A variation of the script displays an JS alert (`js/minitool_dom_patch_with_confirm.js`)

    - A script to set hash value when switching between tabs on a page (`js/minitool_tabhas_bootstrap.js`).

    - 3 frontend solutions to show/reveal more content. (`js/minitool_showhide.js`). Example: an attribite `data-more-close` hides an element by use of jQuery `slideUp` at the page load.

    - A solution to load content into a modal. Content can be cloned from hidden DOM elements of loaded by AJAX (`js/minitool_modal_universal.js`).

## Other, less vital packages & features

    - Translate an address into GPS coordinates thanks to `spatie/geocoder`.

    - Creating expirable links, powered by `spatie/laravel-url-signer`.



# Future features

###Packages installed, but not configured and with no example usage


    - `spatie/laravel-link-checker`.
    - `spatie/laravel-or-abort`.
    - Social logins powered by `laravel/socialite`.
    - caching your queries thanks to `watson/rememberable`.
    - spatie/laravel-analytics
    - spatie/laravel-responsecache
    - unicodeveloper/laravel-password
    - arcanedev/no-captcha
    - arrilot/laravel-widgets
    - classygeeks/potion
    - User-2-user messages, powered by `cmgmyr/messenger`


###Code to write (contributors welcome!): 

    - return to the original page after login

    - User AVATAR supported locally instead of Gravatar - by user's choice

    - spam prevention: blocking certain email domains from registering as users. Sometimes needed to stop bot registration

    - advanced voteup/votedown system provided as an external package

    - solution for storing user options in a separate table linked to User model by hasMany relation


## A list of PACKAGES used in this project
A DB-fed list is available at the 
[DEMO app here](http://dev.unrulynatives.com/package)


    ### this is the `collective` equivalent - used temporarily for the still unreleased Laravel 5.3
        "laravie/html": "~5.3",

    ### Theme system. This App uses it for switching between CSS frameworks
        "igaster/laravel-theme": "~1",

    ### A complete roles/auth solution. 
        "spatie/laravel-permissions": "2.1.*@dev",
        See URL `admintools/assign-roles`


    ### detects if user is using a mobile or a desktop device
        "jenssegers/agent" : "~2.3",

    ### slugs
        "cviebrock/eloquent-sluggable": "dev-master",

    ### a simple admin panel
        "laraveldaily/quickadmin": "^1.1",

    ### tagging for models
        "rtconner/laravel-tagging": "2.*",

    ### comment system
        "slynova/laravel-commentable": "^2.0"
        This system supports replies at multiple level.

    ###Tracking user activity 
     "spatie/laravel-activitylog": "^1.2",
        See URL `admintools/user-track`



## Installation steps

1. Pull the repository to your local drive
2. run `composer install`. You have to install the Composer itself to do that. See [Composer Download Page](https://getcomposer.org/download/).
3. Generate application key with shell command `artisan key:generate`
4. clone the file `.env.example` and rename it to `.env`
5. Create and populate the database. Make sure that 
- you would place the DB credentials to the `.env` file 
    DB_CONNECTION=mysql // this is the default mysql database connection. You can define extra connections later.
    DB_DATABASE=homestead
    DB_USERNAME=homestead
    DB_PASSWORD=secret

- in your `config/database.php` you would make the `mysql` connection refer to your `.env` file.

6. Initiate the Laravel's bundled authentication functions. As described here
use `php artisan make:auth` commmand. 

You would also need to create tables in your database. Use `php artisan migrate` to do that.


### LAST STEP
After completing the above steps the app should work. 
Point your browser to the `localhost/APP_FOLDER/public/`.. You should see the landing page. (This solution required DB connection to work properly)
Point your browser to the `localhost/APP_FOLDER/public/welcome`.. You should see the landing page. (You will see the standard welcome screen delivered by Laravel)



## Contribution guide

Just fork the project, adjust code or provide yours and do a pull request. 


## About this starter package

I am an amateur programmer, trying to create an sophisticated app for decisionmaking. The project is already launched in Poland in 2011. Now the code & content is adjusted to other languages. The gist: the app registers actions of public fugures and other actors present in public space to generate dynamic 'lesser evil' lists for the purpose of voter and consumer decision. The desired functionality is similar to the featured Buycott.com application.

If you like the idea standing behind such an app and are willing to contribute, please contact me.


# About Laravel framework

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell at taylor@laravel.com. All security vulnerabilities will be promptly addressed.



## License

The Laravel framework is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT).
