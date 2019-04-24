# WORDPRESS PLUGIN DEVELOPMENT

Official doc:  
https://codex.wordpress.org/  
https://developer.wordpress.org/plugins/  
https://developer.wordpress.org/reference  


Good resources/tools:

* Plugins: Debug bar
* https://www.rarst.net/wordpress/wordpress-core-load/
* https://www.rarst.net/wordpress/wordpress-query-functions/
* Plugins: query monitor https://es.wordpress.org/plugins/query-monitor/
* http://make.wordpress.org
* Blogs
    * https://managewp.org
    * https://postatus.com
    * https://pippinsplugins.com/blog/
    * https://tommcfarlin.com/
    * https://www.billerickson.net/blog/


## PLUGIN BASICS

### Get started

A plugin can consist of a simple .php file, or a folder containing many files (php, js, css, html, images...)  
However, it's recommended we do it in a folder, just in case we want to expand the plugin in the future

To have a plugin, we need to add this header to the `my-plugin.php` file:

```php
<?php
/*
Plugin Name: WordPress.org Plugin
Plugin URI: https://example.com/plugins/the-basics/
Description: Basic WordPress Plugin Header Comment
Version: 20160911
Author: WordPress.org
Author URI: https://author.example.com/
License: GPL2
License URI: https://www.gnu.org/licenses/gpl-2.0.html
Text Domain: wporg
Domain Path: /languages
*/
```

The plugin can be installed in 2 places:

* wp-content/plugins
* wp-content/mu-plugins

mu-plugins is "must-use". These are activated automatically upon installation

PROs
* are always activated
* cannot be disabled by accident by users
* are loaded before normal plugins
CONs
* no automatic or one-click updates or update notifications
* no activation/deactivation hooks
* single php files only (no folders)

Naming guidelines to avoid incompatibilities

* Research similar names
* Plugin name should match plugin folder and plugin main file names
* Be consistent with naming and KISS

### Explore WordPress APIs

The WP API is comprised of numerous individual APIs, each of which focuses on a specific type of functionality  
https://make.wordpress.org/core/handbook/best-practices/core-apis  
https://codex.wordpress.org/WordPress_API%27s

There are also a bunch of functions and classes readily available in the core:  
https://developer.wordpress.org/reference/

Use these whenever possible, so that WP handles the heavy lifting
Plus, don't reinvent the wheel, there's probably a function already available

Using the WP APIs:

* makes development easier and faster
* ensures backward and forward compatibility
* offers seamless integration with the WP admin area

### Action and Filter hooks

Hooks play a basic role in Plugin development. It's what makes WP so extensible.

There are 2 types of hooks:

* Action hooks = Run Custom Code
    * echo output, write to a file, modify the DB...
* Filter hooks = Modify Data
    * modify post content before sending it to the user...

To use both actions and filters we need a callback function:

```php
function my_callback_function() {
  // code to execute on hook
}
add_action('hook', 'my_callback_function');
```

The order in which actions are executed is here:  
https://codex.wordpress.org/Plugin_API/Action_Reference

Also, there are many filter hooks available:  
https://codex.wordpress.org/Plugin_API/Filter_Reference

Finally, we can add our custom hooks, as well as connect or disconnect existing hooks.

### Plugin activation and deactivation

There are specific hooks that execute when the plugin is:

* activated (`register_activation_hook`)
    * usefule for setting default options, creating specific tables, checking options, etc...
* deactivated (`register_deactivation_hook`)
    * removing temporary data, clearing rewrite rules, delete transients, etc...
* uninstalled (`register_uninstall_hook`)
    * removing plugin data from the database (options in wp_options, ...)


Example (the syntax is the same in all 3 cases):

```php
function my_plugin_on_activation() {

    if ( !current_user_can('activate_plugins')) return;
    // code to execute on activation
}
register_activation_hook( __FILE__, 'my_plugin_on_activation' );
```

### WordPress Pluggable functions

Pluggable functions are functions in the WP Core that can be overwritten by plugin developers.

They are located in `/wp-includes/pluggable.php`

This is how it works. Let's say we want to overwrite the `wp_logout()` function:

```php
if ( !function_exists('wp_logout') ) :
/**
* Log the current user out.
*
* @since 2.5.0
*/
function wp_logout() {
    wp_destroy_current_session();
    wp_clear_auth_cookie();

    /**
     * Fires after a user is logged-out.
     *
     * @since 1.5.0
     */
    do_action( 'wp_logout' );
}
endif;
```

In this case, we could also use the hook created by the `do_action( 'wp_logout' );` sentence. But if we want even more customization (replace the `wp_destroy_current_session();` for example), we can overwrite the function.

What makes this function pluggable is the initial `if ( !function_exists )` condition. To overwrite it, we simply need to redefine the function in our plugin:

```php 
function wp_logout() {   
    // do whatever I want instead
}
```

### Develop secure WordPress plugins

It's very important that we ensure plugins as secure as possible

There is no magic pill. We have to ensure that each variable is sanitized, each user is validated, etc.   
WP provides some guidelines and techniques for:

* data validation
* input/output sanitation
* using nonces
* checking users

https://developer.wordpress.org/plugins/security/

Data validation

* make sure the data is valid
    * (an email address is such, a phone number contains only digits, etc.)
* should be done as early as possible
* should return boolean
* can be done either through
    * WP functions (is_email(), term_exists(), username_exists()...)
    * PHP functions (isset(), empty(), in_array()...)
    * Custom functions

Data sanitization

* make sure data is safe
* it depends on the data context. Not one size fits all...
* can be done either through
    * WP functions (https://developer.wordpress.org/plugins/security/securing-input/)
    * PHP functions (http://php.net/manual/en/filter.filters.sanitize.php)
    * Custom functions

Nonce security

* generated strings used to verify requests for security purposes
* a random number is generated in the form and checked upon submission

### Best practices for Plugin development

Best plugins are compliant to the API and also follow some best practices:

* File organization
    * separate admin assets from public assets
    * put php files in /includes/
    * add propoer header to main file
    * keep root directory uncluttered
        *  plugin-name.php
        *  index.php
        *  uninstall.php
        *  license.txt
        *  readme.txt
* Plugin architecture
    * be organized
    * comment the code
    * will depend on the size/scope of the plugin
    * separate CSS and JS
    * use conditional loading of assets
    * resources
        *  https://iandunn.name/content/presentations/wp-oop-mvc/mvc.php#/
        *  https://jjj.blog/2012/12/slash-architecture-my-approach-to-building-wordpress-plugins/
        *  https://es.wordpress.org/plugins/wp-mvc/
* Avoid naming collisions
    * add a prefix to anything in the public namespace
    * check for existing implementations
        *  variables: isset
        *  functions: function_exists
        *  classes: class_exists
        *  constants: defined
    * use OOP
* Choose a good name: do your research
* Write great documentation
    * https://wordpress.org/plugins/developers/readme-validator/
* Plugin boilerplate
    * http://wppb.io/
    * https://github.com/ptahdunbar/wp-skeleton-plugin
* More best practices



_____________________

## BUILDING A WORDPRESS PLUGIN

### Create the plugin directory and files

We name the plugin "My Plugin"

* /myplugin/index.php
* /myplugin/myplugin.php
* /myplugin/license.txt
* /myplugin/readme.txt
* /my-plugin/admin/
    * /my-plugin/admin/css/
    * /my-plugin/admin/js/
* /my-plugin/public/
    * /my-plugin/public/css/
    * /my-plugin/public/js/
* /my-plugin/includes/
* /my-plugin/languages/


To prevent direct access, we can add this snippet at the beginning of each PHP file:

```php 
// exit if file is called directly
if ( ! defined ( 'ABSPATH' ) ) {
    exit;
}
```


### Add Administration menus

WP gives us 2 choices:

* Top-level menu
    * may contain sub-menus
    * best for plugins with multiple settings pages
* Sub-level menu
    * added to an existing top-level menu
    * best for plugins with only 1 settings page

First we create the settings page:

```html
<?php
// display the plugins settings page
function my_plugin_display_settings_page() {
    // check if user is allowed access
    if ( ! current_user_can('manage_options') ) {
        return;
    }

?>

<div class="wrap">
    <h1><?php echo esc_html( get_admin_page_title() ); ?></h1>
    <form action="options.php" method="post">
<?php
// output security fields
settings_fields('myplugin_options'); // must match the ID of register_settings()

// output settings sections
do_settings_sections('myplugin');    // slug

// submit button
submit_button();
?>

    </form>
</div>

<?php
}
```

And then we add a menu link - TOP LEVEL

```php
// add top level administration menu
function myplugin_add_toplevel_menu() {
    add_menu_page(

        /*
        * string $page_title,
        * string $menu_title,
        * string $capability,
        * string $menu_slug,
        * callable $function = '',       -> callback function that displays the page
        * string $icon_url = '',
        * int $position = null
        */

        'MyPlugin Settings',
        'MyPlugin',
        'manage_options',
        'myplugin',                             // slug
        'my_plugin_display_settings_page',
        'dashicons-admin-generic',
        null
    );
}
add_action( 'admin_menu', 'myplugin_add_toplevel_menu' );
```

or - SUB LEVEL

```php
// add sub level administration menu
function myplugin_add_sublevel_menu() {
    add_submenu_page(

        /*
        * string $parent_slug,
        * string $page_title,
        * string $menu_title,
        * string $capability,
        * string $menu_slug,
        * callable $function = '',
        */

        'options-general.php',
        'MyPlugin Settings',
        'MyPlugin',
        'manage_options',
        'myplugin',
        'my_plugin_display_settings_page'
    );
}
add_action( 'admin_menu', 'myplugin_add_sublevel_menu' );
``` 

### Add the plugin settings page

We do this through the Settings API, which provides security and consistency  
https://developer.wordpress.org/plugins/settings/settings-api/  
https://codex.wordpress.org/Settings_API

First thing is to plan the setting pages needed. In our case we will need 2:

* one to customize the login page
* one to customize the admin area


In the end, it's mostly about building forms with:

* text input `<input type="text">`
* radio input `<input type="radio">`
* checkbox `<input type="checkbox">`
* textarea `<textarea>`
* select menu `<select>`

To add a setting:

1. create a function to register the setting options, sections and fields, and hook it in `'admin_init'`
2. register the setting options via the `register_setting()` function
3. add sections via the `add_settings_section()` function
4. add fields to each section via the `add_settings_field()` function


#### STEPS 1 and 2

```php
// register plugin settings
function my_plugin_register_settings() {

register_setting(
    'myplugin_options',                                                                      // ID
    'myplugin_options',
    'myplugin_callback_validate_options'
);
}
add_action('admin_init', 'my_plugin_register_settings');
```
-> + need to define the callback function

#### STEP 3
```php
add_settings_section(
    'myplugin_section_admin',   // ID
    'Customize Admin Page', // title of the section
    'myplugin_callback_section_admin',  // callback function with description of the section     
    'myplugin'                                                                    // must match the slug defined in the admin menu registration
);
```
-> + need to define the callback function


#### STEP 4

```php
add_settings_field(
    'custom_url', // setting ID, used when retrieving from the DB
    'Custom URL', // title of the setting, displayed on the page
    'myplugin_callback_field_text', // callback function, contains the markup to display the setting
    'myplugin', // slug of the page to display the field
    'myplugin_section_login', // section ID where to display the field ( defined in add_settings_section() )
    [ 'id' => 'custom_url', 'label' => 'Custom URL for the Login logo link'] // array that contains any data we want to pass to the                 callback function
);
```
-> + need to define the callback function

### Add settings callback functions

Next step is to write the callback functions

First, we define a function with the default options

then, we add the code for each callback function

### Validate plugin settings

We write the function `myplugin_callback_validate_options()` to validate/sanitize all the inputs   
This is the callback for the `register_setting()` function

### Add custom functionality

Now we want to add the actual functionality for each of the settings (ie: customize the login URL)

We add them in `includes/core-functionalities.php`, since they will be accessed for both admin and front panels

Basically, for each option/setting, we add a hook (action/filter) that does what is promised

### Include JavaScript and CSS

In this video, we build the custom functionality for the "custom style" setting

When this option is selected, the plugin will include a custom CSS and JS on the login page with `wp_enqueue` in the login page hook

### Plugin internationalization

General steps:

1. prepare folders and files
    1. add a languages/ folder
    2. use the same slug for main folder and file
    3. add "text domain" and "domain path" to plugin header
2. add localization functions
    1. include `load_plugin_textdomain()`
    2. replace all text strings with a localization function
3. generate the POT file


**2.1) include load_plugin_textdomain()**

```php
function myplugin_load_textdomain() {
     load_plugin_textdomain( 'myplugin', false, plugin_dir_path( __FILE__ ) . 'languages/' );
}
add_action('plugins_loaded', 'load_plugin_textdomain');
```

**2.2) to internationalizea string**
```php
__( 'string to translate', 'myplugin_textdomain');
```
We only need to translate those strings that will be seen by the user

Alternatively:

* _e() - echo instead of return
* _x() - provides extra parameter for context
* or with sanitization:
    * esc_html__()
    * esc_html_e()
    * esc_html_x()


**3) the POT file**

Is a template translators will use when translating the plugin we can generate it with poedit, or with Loco Translate plugin


### Add an uninstall feature

Good plugins clean up after themselves: delete options and temporary data are removed from the database

There are 2 techniques:

* use `register_uninstall_hook()` 
* use a file `uninstall.php` (preferred)


Option 1:

```php
function myplugin_on_uninstall() {

     if (! current_user_can('activate_plugins') ) return;
     delete_option( ''my_plugin_options );
}
 register_uninstall_hook( __FILE__, 'myplugin_on_uninstall') 
```

Option 2:

When addedtothe main directory, the uninstall.php will be arun automatically when the plugin is uninstalled

```php
if( ! defined ( 'WP_UNINSTALL_PLUGIN' ) ) {
     exit;
}
delete_option( ''my_plugin_options );
```

Other deletion options:

* delete_option()
* delete_site_option()
* delete_transient()
* delete_metadata()
* delete database table:

```php
global $wpdb;
$table_name = $wpdb->prefix . 'table_to_delete';
$wpdb->query( "DROP TABLE IF EXISTS {$table_name}" );
```
* delete cron event:

```php
$timestamp = wp_next_scheduled( 'sfs_cron_cache' );
wp_unschedule_event( $timestamp, 'sfs_cron_cache' );
```


### Test and debug

https://codex.wordpress.org/Debugging_in_WordPress  
https://developer.wordpress.org/plugins/developer-tools/


Add in wp-config.php

```php
// enable debug 
define('WP_DEBUG', true);

// log debug info
define('WP_DEBUG_LOG', true);

// display debug info
define('WP_DEBUG_DISPLAY', false);

// save queries
define('SAVEQUERIES', false);
```

Tips:

* test extensively as you develop
* test in different installations (local and remote)
* test internationalization on an installation in a foreign language
* test compatibility with other plugins (most popular, related plugins, etc.)
* plugin helper
    * https://wordpress.org/plugins/query-monitor/
    * https://wordpress.org/plugins/developer/
* other
    * include the no-direct-access code to non empty PHP files
    * properly namespace all public functions, classes, etc
    * delete any empty folders and files




______________________________

## ESSENTIAL PLUGIN TECHNIQUES

### Customize the WordPress loop

The WP Loop is a piece of code that loops through posts and displays them on the Front-End
https://codex.wordpress.org/The_Loop  
https://codex.wordpress.org/The_Loop_in_Action  
https://developer.wordpress.org/themes/basics/the-loop/  
https://digwp.com/2011/05/loops/

```html
<?php if (have_posts()) : ? ?>
    <!-- markup/tags to be displayed only once -->

    <?php while (have_posts()) : ?>

        <?php the_post(); ?>
        <!-- markup/tags used to display each post -->
    <?php endwhile(); ?>

    <!-- markup/tags to be displayed only once -->

<?php else : ?>
    <!-- markup/tags when no posts are found -->

<?php endif; ?>
``` 

Basically there are 3 tecniques used for custom loops:

* `get_posts() - useful for creating sidebar loops
* `pre_get_posts() - useful for customizing the main loop
* `WP_Query` - useful for creating custom loops and multiple loops. This is the most flexible/customisable


The video shows an example of custom loops using shortcodes  
--> SEE AGAIN


### Create widgets

Widgets enable users to add content and display information on the front-end of the site

Here we see how to create custom widgets available to our plugin  
https://codex.wordpress.org/Widgets_API

We create a widget by extending the `WP_Widget` class

In the video there is a tutorial for creating a widget, also available here:  
https://perishablepress.com/clean-markup-widget/


### Manage users and roles

User's data is stored in the database table *`users`*
Each user has at least a username, password and email

To create a user:

```php
wp_create_user(
     string $username,
     string $password,
     string $email
);
```
There is also a more advanced function: `wp_insert_user();`

We can also update existing users with `wp_update_user()` and delete with `wp_delete_user()`

To add a new role we use `add_role()`  
To remove an existing role: `remove_role()`  
To get a role: `get_role()`


### Work with JavaScript and CSS

WordPress provides numerous functions to include JS and CSS. In this tutorial we focus on:

* CSS
    * `wp_enqueue_style()`
    * `wp_add_inline_style()`
* JS
    * `wp_enqueue_script()`
    * `wp_add_inline_script()`


To enqueue scripts and styles in the admin area, we use the hook `'admin_enqueue_scripts'`

To enqueue scripts and styles in the front site, we use the hook `'wp_enqueue_scripts'`

To enqueue scripts and styles in the login page, we use the hook `'login_enqueue_scripts'`

Only thing is that, in order to ad dinline styles/scripts, we must first add them through `wp_enqueue`, so that to have the same ID (`'myplugin-public'`)

Finally, besides adding our sctriipts/styles, we can also register them for use within other functions in our plugin:

* `wp_register_script()`
* `wp_register_style()`

### Use the Options API

We can use the Options API to add/remove/update our Plugin options:

* `get_option()`
* `add_option()`
* `update_option()` 
* `delete_option()` 


The options API is a simpler alternative to the Settings API. It's easier to CRUD the database, but the Settings API provides a more consistent interface (validation + sanitization + visual consistence)

Basically: Options API is a database API, whereas Settings APi is more an interface API




______________________

## EXTENDING PLUGIN FUNCTIONALITIES

### Add custom post types and taxonomies

Here we see just an overview. For more details, check the other course  
https://www.lynda.com/WordPress-tutorials/WordPress-Custom-Post-Types-Taxonomies/163113-2.html

WP includes several default post types:

* post
* page
* attachment
* revision
* menu

And defulat taxonomies:

* category
* post_tag
* link_category
* post_format


We create a callback function that registers the post types, and hook it to the `'init'` hook, which is launched on all pages, both admin and public

This automatically creates an interface in the menu to create new posts of this CPT


### Work with custom fields

Custom fields are a type of metadata linked to posts, users, comments and terms:

* get_post_meta()
* get_user_met()
* get_comment_meta()
* get_term_meta()

Meta data for posts is aka "Custom fields"
Custom fields consist of key-value pairs, where key names can be used more than once

In the Admin Area, CF are displayed in a specific meta box named "Custom Fields"
CFs can be added by plugins, or directly by the user


### Add meta boxes

Meta boxes are sections within the admin post edit's page post.php  
Meta boxes contain some HTML and/or form data, but no Submit button. The Submit is the "Update Post" button

Meta boxes allow us to add metadata to our posts or CPTs in a cinvenient way, as meta boxescan be displayed, hidden, rearrangeable, etc...


### Work with custom database queries

WP provides a whole set of functions that we can use to interact with the DB. And in case we don't find we need, we even have the possibility to add custom queries through the global $wpdb instance of the wpdb class

To do so, declare and use the global variable:

```php
function myplugin_database_query( $query ) {
     global $wpdb;
     $results = $wpdb->get_results( $query );
     return $results;
}
```

The `wpdb` class provides many methods:  
https://developer.wordpress.org/reference/classes/wpdb/#methods

| Method | Description 
| --- | ---
| `$wpdb->prepare()` | Escape a SQL query (SQL injection protection)
| `$wpdb->get_results()` | Get generic results
| `$wpdb->get_var()` | Get a variable
| `$wpdb->get_col()` | Get a column
| `$wpdb->get_col_info()` | Get column information
| `$wpdb->get_row()` | Get a row
| `$wpdb->insert()` | Insert row

Steps:

1. define the query
2. replace the variable with a placeholder
3. prepare the query
4. execute the query


### Integrate admin notices

Admin notices are displayed on the top of the pages in the admin area  
Admin notices are important as a way to inform the user about things that happen behind the scenes

There are 2 scenarios for admin notices:

* If the plugin settings are located in the default Settings menu, notices are managed automatically by WP
* Otherwise, we have to manage them in our plugin, through the settings_errors() function

Also, we can create our custom notices in a callback function and hook it in 'admin_notices'

Use the recommended classes to keep notices consistent with the default look&feel



___________________________

## ADVANCED PLUGIN TECHNIQUES

### Use the Transients API

The Transients API allows to store temporary data in the WP database (*options* table)


### Use the HTTP API

The HTTP API allows to make HTTP requests to let WP interact with other API (Twitter, Facebook, Google Maps, etc)  
https://codex.wordpress.org/HTTP_API  
https://developer.wordpress.org/plugins/http-api/

Basics of HTTP:

* There are several types of request methods
    * GET
    * POST
    * HEAD
    * etc.
* HTTP status codes (response codes)
    * 1xx - custom status codes
    * 2xx - request successful
    * 3xx- request redirected to another URL
    * 4xx - request faileddu to client error
    * 5xx - request failed due to server error


There are several functions available in the HTTP API. These functions return either the status code, or an error message

-> NOT FINISHED



### Use WP-Cron

The WP-cron API is a pseudo cron service, that runs on each page load  
It requires a page load to work

Unlke Unix cron, that is constantly running, WP-cron runs only on page load, checks for jobs with past scheduled time, and launches them

For most cases, this approach can work well, but for sites with little activity, it might not be suitable


### Implement AJAX

WP provides built-in AJAX functionality

For that we need to load a .js file containing AJAX queries into our page(s)


### Use the REST API



_________________________________________
_________________________________________

# WORDPRESS: ACTION AND FILTER HOOKS

## UNDERSTANDING HOOKS AND FILTERS

### What is WordPress?

Open source software built on PHP and MySQL

2 flavors:

* .org
* .com

There are 2 ways in which developers can interact with WP:

* themes -> layout and design
* plugins -> functionality


### What is the Plugin API?

A Plugin is a set of functions written in PHP that add specific features or services to a WP site  
WP provides its API through a set of hooks (actions and filters), that allow us to latch onto WP at a specific point in runtime  
The API is the set of instructions WP provides to let us interact with its core.


### Action hooks explained

Action hooks are used to add, modify or remove functionality

Here we have the list of available action hooks:  
https://codex.wordpress.org/Plugin_API/Action_Reference

And also, we have a set of available functions to work with action hooks:

* has_action() - checks if any action has already been registered for a particular hook
* add_action() - hook a function to the action hook
* do_action() - add a new hook tag => call functions registered on a particular hook
* do_action_ref_array()
* did_action()
* remove_action() - opposite to add_action()
* remove_all_actions()
* doing_action()

Action hooks are created in WP with the `do_action('hook_name')` function

Functions are hooked with the `add_action('hook_name', 'callable_function')` function


### Filters explained

Filter hooks are used to take some data, modify it (apply a filter on it), and then return it  
Filters sit between the database and the browser, in any direction

This is the list of available filter hooks:  
https://codex.wordpress.org/Plugin_API/Filter_Reference

Like for actions, there are a set of filter functions available:

* has_filter() - checks if any filters have been registered for a hook
* add_filter() - hook a function to the filter hook
* apply_filters() - call all filters registered on a filter hook (equivalent to do_action)
* apply_filters_ref_array()
* current_filter()
* remove_filter()
* remove_all_filters()
* doing_filter()


### Priorities

When working with hooks, WP provides priorities and arguments for us.   
Lower priorities happen earlier. Default is 10.   
If I want to hook in between 2 hooks already existing with a priority of 10, for example,I have to remove one of them and rehook it with another priority  
Important: when removing, we have to specify the priority


### Arguments

Integer optional passed to add_action() and add_filter()  
Number of arguments expected in the callable function (default is 1)



_______________________

## HOOKS AND FILTERS IN ACTION

### Customizing the WordPress login page

Create a new plugin


### Adding a custom stylesheet

* we go to `wp-login.php`, which is the file that powers the login page
* we see there is a `do_action('login_enqueue_scripts')`
* we create a function in our plugin that hooks in there and calls `wp_enqeue_style()`


### Filtering login error messages

* we go to `wp-login.php`, which is the file that powers the login page
* we see there is an `add_filter('login_errors')`
* we create a function in our plugin that hooks in there and filters the message

If we wanted to return nothing, we could pass "__return_null" instead of the callable


### Remove the login page shake

* we go to `wp-login.php`, which is the file that powers the login page
* we see there is an `add_action('login_head', 'wp_shake_js')`
* we create a function in our plugin that removes that action

Note that we cannot call `remove_action()` directly, we have to call it inside a callable, and hook that callable in `'login_head'`



_____________________

## WORKING WITH HOOKS AND FILTERS

### Finding references and documentation

This is a good reference  
https://codex.wordpress.org/Plugin_Resources  
https://developer.wordpress.org/plugins/

And of course Google

Beware that this is an open source project, and therefore maintained by volunteers. So sometimes we may encounter errors. It's not usual, but just to keep in mind

There might be a package for our IDE or code editor that includes WP functions


### Identifying available hooks and filters

In the Plugin API wiki we have a good reference. Don't hesitate to google, or even refer to the code (search for do_action() and apply_filter())

Also recommended: Debug Bar plugin + Addon Actions and Filters -> this shows on every page the hooks available


### A look at load order

In the Plugin API the available hooks are listed in approximate load order  
Order is very important because we want to inject our code at the right point at runtime

https://es.wordpress.org/plugins/query-monitor/


### Understanding callback functions

A callback function is a function that is passed as an argument to another function

It doesn't matter where we write our callback function, doesn't need to be next to add_action, but typically it is


### Using apply_filters

This allows someone else to do an add_filter('vip_list', $new_list) and edit my initial list

```php
function invitation_list() {
    $guests = array( 'Carrie', 'Major', 'Bert');
    $guests = apply_filters( 'vip_list', $guests );
    return $guests;
}
```


### WP_Hook vs. $wp_filter

Before, there was an array $wp_filter that stored all the hooks and callbacks  
But there was a bug with recursive callbacks, so the $wp_filter variable was replaced with the WP_Hook class  
More info:  
https://deliciousbrains.com/hooks-line-sinker-wordpress-wp-hook-class/

Most probably we'll never need to deal with these variables if we work with the Plugin API, but good to know



___________________________

## WORKING WITH NON-WORDPRESS HOOKS

### Adding custom hooks

Creating our own hooks is pretty easy with the `apply_filters` and `do_action` functions  
This may be interesting when we develop themes or plugins

Examples:

```php
/**
* Plugin Name: Your Plugin
*/
function top() {
    return apply_filters( 'top-text', 'This is the top' );
}
echo top();

do_action( 'in_the_middle' );

function bottom() {
    return 'This is the bottom';
}
echo bottom();

/**
* Plugin Name: My Plugin
*/
add_action( 'in_the_middle', 'something' );
function something() {
    echo 'This is the middle';
}

add_filter( 'top_text', 'change_top_text' ):
function change_top_text() {
    return 'This is the tippity top!!';
}
```

Be cautious: if we add hooks and other developers use them, we cannot remove them anymore if we want to maintain backwards compatibility  
A good rule of thumb is to add them if other developers ask us to


### Inside themes and plugins with hooks

A lot of large plugins (Woocommerce, BuddyPress) and theme frameworks (Genesis) have hooks built in  
https://carriedils.com/genesis-hook-reference/  
https://genesistutorials.com/visual-hook-guide/


### Tips for using third-party hooks

Best practices when using 3rd party hooks in our own plugins

* If our plugin is dependent on another plugin/theme, check if that one is activated and if not, display an error message
* Check for dependencies before using a hook
* Be aware of updates in their libraries
* Document your source code

https://make.wordpress.org/core/handbook/best-practices/inline-documentation-standards/



______________________

## BUILDING A DEMO PLUGIN

### A look at what you're building



### Setting up the folder and file structure

* create main php file
* stylesheet


### Registering a sidebar

```php
add_action( 'widgets_init', 'spcp_register_sidebar');
/**
* Registers a sidebar called Post Content Plus.
*/
function spcp_register_sidebar() {
     
          register_sidebar( array(
               'name'               => __( 'Post Content Plus', 'spcp'),
               'id'               => 'spcp-sidebar',
               'description'      => __( 'Widgets in this area display on single posts', 'spcp' ),
               'before_widget'     => '<div class="widget spcp-sidebar">',
               'after_widget'     => '</div>',
               'before_title'     => '<h2 class="widgettitle spcp-title">',
               'after_title'     => '</h2>',
          ) );
}
```


### Displaying a sidebar on single posts

We use the function dynamic_sidebar. The is_main_query condition is to make sure we dont interfere with other plugins

```php
add_filter( 'the_content', 'spcp_display_sidebars' );
/**
* Display sidebar on single posts.
* 
*/
function spcp_display_sidebars( $content ) {
     if ( is_single() && is_active_sidebar( 'spcp-sidebar' ) && is_main_query()  ) {
          dynamic_sidebar( 'spcp-sidebar' );
     }
     return $content;
}
```


### Applying filters for loading stylesheets

```php
add_filter( 'spcp_load_styles', '__return_false' );`
```

### Putting it all together

```php
<?php
/**
* Plugin Name:     Single Post Content Plus
* Description:     Adds a sidebar/widget aka to single posts.
* Version:          0.1.0
* Author:          Carrie Dils
* Author URI:     https://carriedils.com
* Text Domain:     spcp
* License:          GPL-2.0+
* Github Plugin URI:     https://github.com/cdils/single-post-content-plus
*/

// If this file is called directly, abort
if ( !defined('ABSPATH') ) {
     die;
}

add_action( 'wp_enqueue_scripts', 'spcp_login_stylesheet' );
/**
* Load plugin styles.
*
*/
function spcp_login_stylesheet() {
     if ( apply_filters( 'spcp_load_styles', true ) ) {
          wp_enqueue_style( 'spcp-custom-stylesheet', plugin_dir_url(__FILE__) . 'spcp-styles.css' );
     }
}


// Uncomment the following line to keep spcp-custom-stylesheet from loading
// add_filter( 'spcp_load_styles', '__return_false' );
add_action( 'widgets_init', 'spcp_register_sidebar');
/**
* Registers a sidebar called Post Content Plus.
*/
function spcp_register_sidebar() {
    
          register_sidebar( array(
               'name'               => __( 'Post Content Plus', 'spcp'),
               'id'               => 'spcp-sidebar',
               'description'      => __( 'Widgets in this area display on single posts', 'spcp' ),
               'before_widget'     => '<div class="widget spcp-sidebar">',
               'after_widget'     => '</div>',
               'before_title'     => '<h2 class="widgettitle spcp-title">',
               'after_title'     => '</h2>',
          ) );
}


add_filter( 'the_content', 'spcp_display_sidebars' );
/**
* Display sidebar on single posts.
*
*/
function spcp_display_sidebars( $content ) {
     if ( is_single() && is_active_sidebar( 'spcp-sidebar' ) && is_main_query()  ) {
          dynamic_sidebar( 'spcp-sidebar' );
     }
     return $content;
}
```


_____________

## CONCLUSION

### Stay up to date with WordPress development

WordPress is ever evolving. The WP development team always buils on top on each release, never replaces.

Stay ware on thelatest news and features:
* http://make.wordpress.org
* https://managewp.org
* https://postatus.com




_____________________________
_____________________________________________

# WORDPRESS: CUSTOM POST TYPES

## UNDERSTANDING CUSTOM POST TYPES AND TAXONOMIES

### What are Custom Post Types and Taxonomies?

**Post types**

Out of the box, WP provides several post types. 

* posts
* pages
* attachments
* menus
* etc.


The most common are Posts and Pages

* Posts
    * reversed chronological
    * non-hierarchical
    * author
    * must have a category
    * can have tags
    * can have archie/index
* Pages
    * single items
    * parent-child relationship
    * dont have index or taxonomies

**Custom post types**

* can act as posts or pages
* can have a combination of post/pages features
* can be called anywhere using a custom loop

**Taxonomies**

* a scheme for classification
* an organizational system that allows to relate one item with other similar in hierarchical or non-hierarchical groups


In WP there are 2 default taxonomies

* categories
    * mandatory for posts
    * hierarchical
* tags
    * optional
    * non-hierarchical


**Custom taxonomies**

* can be hierarchical or non-hierarchical
* can be applied to any post type (also posts/pages)
* can have custom archive templates


### Where does the CPT and Taxonomy code belong?

We have 2 options:

* plugin
    * best for most situations
    * theme-independent
    * can be turned on/off
* theme
    * only for custom theme build
    * theme-dependent
    * allows for more advanced taxonomy



________________________

## CREATING A PLUGIN FOR CUSTOM POST TYPES AND TAXONOMIES

### Creating a basic plugin

Just create the php file


### The no-code solution: The Custom Post Type UI plugin

If we just want to quickly set up our CPTs and don't need advanced custom features, maybe a plugin likt CPT-UI may be a good solution  
https://wordpress.org/plugins/custom-post-type-ui


### Create custom post types (CPT UI plugin)

To create a CPT with the plugin:

* Add new
* Fill in basic info
    * slug
    * Plural label
    * Singular label


### Customize custom post type labels (CPT UI plugin)

Technically, all we need to create a new CPT is the slug, plural label and singular label

But beyond this, we can edit some additional labels. In the plugin they are pretty much well explained

Advise is to customize all of them

Note that all these labels are for the admin backend only


### Customize the Custom Post Type UI settings

With the settings, we can customize how the CPT appears on the backend,what is available from it in the front end, and what features it has

* public: whether the CPT is avilable on the front end
* Publicly Queryable: whether the CPT can be queries from the FE
* Show UI: the opposite, whether it is available in the admin panel
* Show in Nav menus: available for WP front-end menus
* Show in REST API
* Has archive: does the CPT have its own archive index page
* Exclude from Search: not want index it
* Capability type: post, page, etc (refer to codex)
* Rewrite: if FALSE, the URL will be a GET query from database, so almost always put to YES
    * do not change it afterwardsor it wil lbreak all the links
* With Front: whether or not the post type is listed in the URL /testimonials/
* Query Var: normally yes
* Menu position: where in the admin menu will our CPT menu appear
* Menu icon: which icon to display in admin menu
* Supports: features available in the CPT post editor
* Custom supports: we can add features through plugins, etc. (advanced)
* Built-in taxonomies: if we want to apply any taxonomies


### Create custom taxonomies (CPT UI plugin)

By default, WP have 2 taxonomies: Categories and Tags

To create a Custom Taxonomy with the plugin:

* Add new
* Fill in basic info
    * slug
    * Plural label
    * Singular label
    * Attach to type (taxonomies must always be attached to a post type)


### Customize custom taxonomy labels (CPT UI plugin)

Taxonomies operate similarly to CPTs

We can also edit all the labels through the plugin


### Customize custom taxonomy settings (CPT UI plugin)

Most of the settings are the same as for CPTs

Specific settings:

* Hierarchical (TRUE-> like categories / FALSE-> like tags)
* Show admin column: whether it appears as a column on the post list in the admin panel
* Show in quick/bulk edit panel


### Export and import custom post types, taxonomies and settings (CPT UI plugin)

We can Delete post types in the tab "Edit Post Types". Note this will not delete the CPT from the database, that has to be done manually. It only deletes the access menus in the admin panel (removes register functions)

We can also access to the PHP code,either to:

* save it for backup
* export/import to another WP site
* copy/paste directly in a plugin or functions.php and remove the CPT UI plugin

This can also serve as a basis to generate the boilerplate code for our CPTs and then generate the code and delete the plugin if we want to



________________________

## CREATING CUSTOM POST TYPES

### Creating a basic CPT

Out of the box, WP has 5 default post types:

* posts
* pages
* attachments
* revisions
* menus

These are nothing more than CPTs. This show how advanced CPTs are. We can manage almost any type of content.

We create CPTs with the register_post_type() function. It accepts 2 arguments: 

* The CPT slug
* A list of arguments that define the labels and settings of the CPT

We call this function inside a callback that we hook to 'init':

```php
function my_custom_posttypes() {

     // inside here we can create (register) as many post types as we want. For example:
     $args = array(
          'public' => true,
          'label' => 'Testimonials'
     );
     register_post_type( 'testimonials', $args );

}
add_action( 'init', 'my_custom_posttypes' );
```

### Building out an advanced CPT

https://codex.wordpress.org/Function_Reference/register_post_type
https://developer.wordpress.org/reference/functions/register_post_type/

Basically, copy/paste from the codex and suctomize the settings and labels we want

One thing he does is to do a flush rerite upon plugin activation


### Testing the CPT in WordPress admin

Go through the admin panel to check the plugin behaviour


### Make CPTs available from the REST API

There are 3 arguments in the RPT array:

* show_in_rest -> boolean, activate/deactivate the Rest API for our CPT
* rest_base-> if we want to change the base slug for our CPT. Advice: leave it the same
* rest_controller_class -> advanced feature (check codex)


### Challenge: Create a CPT for reviews

Not interesting, just copy/paste


### Creating posts with CPTs

Create a few posts of each type



_________________________

## CREATING CUSTOM TAXONOMIES

### Creating basic custom taxonomies

Out of the box, WP links all our posts using 2 types of taxonomies:

* categories (hierarchical)
* tags (non-hierarchical)

But in many cases, these two are not enough

We can create custom taxonomies in a much similar way to CPTs

We use the register_taxonomy() function. It accepts 3 arguments: 

* The taxonomy slug
* The list of post types it should apply to (can be an array)
* A list of arguments that define the labels and settings of the CPT

We call this function inside a callback that we hook to `'init'`:

```php
function my_custom_taxonomies() {

     // inside here we can create (register) as many post types as we want. For example:
     $args = array(
          'label' => 'Type of Product / Service'
          'rewrite' => array( 'slug' => 'product-types' ),
          'hierarchical' => true,
      );
     register_taxonomy( 'product-type', 'reviews', $args );

}
add_action( 'init', 'my_custom_taxonomies' );
```

### Building out advanced custom taxonomies

https://codex.wordpress.org/Function_Reference/register_taxonomy
https://developer.wordpress.org/reference/functions/register_taxonomy/

Basically, copy/paste from the codex and customize the settings and labels we want

There is a lon list of reserved taxonomies (reserved terms). Beware not to use that same name (ex: day, year, ...)


### Make custom taxonomies available from the REST API

Just like CPTs, custom taxonomies can also be made available to the REST API

There are 3 arguments in the RPT array:

* show_in_rest -> boolean, activate/deactivate the Rest API 
* rest_base-> if we want to change the base slug. Advice: leave it the same
* rest_controller_class -> advanced feature (check codex)


### Applying custom taxonomy terms to posts

Create a few taxonmies of each type and assign them to existing post types



_________________________

## CREATING CUSTOM POST TYPE TEMPLATES

### Exploring the WordPress template hierarchy

https://developer.wordpress.org/files/2014/10/wp-hierarchy.png

The template hiwerarchy allows us to provide a cusotmized experience for each of ourCPTs or custom taxonomies

This way we can display the contents of a CPTs differently from a default post or page


### Creating a single post template for a CPT

We create a file named `single-mycpt.php`  
We can start off from single.php. Depending on the theme, the contents of the file will change


### Adding custom taxonomies to a template

We hve to look our current template `single-mycpt.php` and modify it accordingly

Useful functions:

* get_the_terms
* get_the_term_list


### Creating a taxonomy archive template

Archive templates are handled by default with archive.php

To target a custom taxonomies we can create a new file taxonomy.php, or even taxonomy-mycustomtaxonomy.php
We can start off from archive.php. Depending on the theme, the contents of the file will change

Useful functions:

* get_queried_object
* get_taxonomy


### Creating a CPT index page

This template file displays a list of our CPTs, in the same way blog.php displays the list of our post entries
We can customize it depeding on the theme




_____________________

## WORKING WITH CUSTOM POST TYPES AND TAXONOMIES

### Including CPTs in the front-page index

We add in functions.php:

```php
function my_add_reviews( $query ) {

     if ( !is_admin() $$ $query->is_main_query() ) {    

          if ($query->is_home()) {
               $query->set( 'post-type', array('post', 'reviews' ) );
          }
     }
}
add_action( 'pre_get_posts', 'my_add_reviews' );
```

What this does is to intercept the query with pre_get_posts hook. And in teh query, mix both regular posts and reviews, but making sure it's only on the front page when set as blog page  
`pre_get_posts()` can affect the main query all over our site


### Identify a CPT in index pages and search results

He uses this:

```php
if ( 'reviews' == get_post_type() ) {
     echo '<div class="reviews-header">Review</div>';
}
```


### Creating custom loops for custom post types

He uses `wp_reset_query()` to restore the main query. 
However, official documentation says to use `wp_reset_postdata()` instead  
https://codex.wordpress.org/wp_reset_postdata




_______________________

## TYING CUSTOM POST TYPES AND TAXONOMIES TO A THEME

### Add CPTs and Taxonomies to a theme

We have to put the code in `functions.php`, or in a separate file that we call include in `functions.php` with

```php
require get_stylesheet_directory() . '/my-file.php';
```


### Initialize CPTs on theme activation

Add this :

```php
function my_rewrite_flush() {
    my_custom_posttypes();
    flush_rewrite_rules();
}
add_action( 'after_switch_theme', 'my_rewrite_flush');
```


__________________________________
__________________________________

# WORDPRESS CHILD THEMES WITH GENESIS


## EXPLAINING GENESIS AND WORDPRESS

### The core of the Genesis Framework

In `lib/framework.php` is defined the function genesis(); the core of the framework

Structure

* config - config files, contributors
* images - logo and favicon
* lib - the guts of Genesis
    * admin - all the code for the WP admin area
    * classes - PHP POO classes
    * css
    * functions - helper functions
    * js
    * languages - for translation files
    * shortcodes
    * structure - defines the layout
    * views - HTML views 
    * widgets - code for widgets
* root directory
    * template files


### Template files in the Genesis Framework

The template files are contained in the root directory

Unlike other themes, the Genesis templates have very little code


### Understanding the child theme template structure

Normally in a WP child theme, we would copy the files we want to override from parent to child

In Genesis, since it's based in hooks, we only need (in theory) two files:

* functions.php
* style.css

Now Genesis Sample provides support for Woocommerce


### What is the WordPress loop?

https://codex.wordpress.org/The_Loop  
https://codex.wordpress.org/The_Loop_in_Action  
https://developer.wordpress.org/themes/basics/the-loop/

It's WordPress process that loops over every post to display them

It's always the same loop used. Whether it displays 1 post or all the posts, depends on the context where it is used. And this context comes form the WordPress template hierarchy:  
https://developer.wordpress.org/themes/basics/template-hierarchy/#visual-overview

This hierarchy shows the template files we can use in a theme, and the order in which WP looks for them

So we can get as specific as we want, and WordPress will automatically determine the right context of posts to display in the default loop



### What is the Genesis loop?

We can also alter the loop  
The Genesis loop works the same logic as the std WP loop, but additionally provides the ability to hook anywhere in the loop

It is defined in `genesis/lib/structure/loops.php`

Here are defined several loops:

* genesis_standard_loop - the standard WP + Genesis actions/hooks
* genesis_custom_loop - used occasionally
* genesis_legacy_loop - ignore it. XHTML backwards compatibility
* genesis_grid_loop - ignore it. backwards compatibility



### Action hooks and filters in WordPress

The WordPress Plugin API provides actions and hooks that allow developers to interact with WP  
https://codex.wordpress.org/Plugin_API

Hooks are spread all over WP process and allow us to introduce our custom code

Genesis provides a similar functionality in the sense it allow customizations by hooking into the theme

Hooks come in one of two flavours:

* Action hooks - points in the WP lifecylce that allow you to ad, remove or modify certain functionality
* Filter hooks - points in the WP lifecylce that allow you to ad, remove or modify certain data


There are many actions and filters available:  
https://codex.wordpress.org/Plugin_API/Action_Reference  
https://codex.wordpress.org/Plugin_API/Filter_Reference



### Action hooks and filters in Genesis

https://genesistutorials.com/visual-hook-guide/

The basic idea is that if we want to change the place of something, it's a 2 step:

1. `remove_action('old_where', 'what');`  
2. `add_action('new_where', 'what');`

> NOTE: The `apply_filter()` function defines where we can modify through a filter



________________________

## EDITING THEME FILES

### Editing the style sheet

It's in `child-theme/style.css`

Recommendation is to put all CSS in here

Where in the file is personal preference, either all grouped together, or in the appropriate sections of style.css


### Working with functions

it's in `child-theme/functions.php`

Be careful here, a typo in functions.php can break our site

We can add conditionals to display based omn certain conditions, pages, etc  
Check list of conditional tags:  
https://codex.wordpress.org/Conditional_Tags



### Adding a custom header image

In functions.php

```php
add_theme_support(
    'custom-logo',
    array(
        'height' => 120,
        'width' => 700,
        'flex-height' => true,
        'flex-width' => true,
    )
);
```
Then go to style.css and modify in there (using Inspector to see where)


### Customizing the footer credits

There are a lot of snippets in   
https://my.studiopress.com/documentation/snippets/

NOTE: 

* add_action does something
* add_filter returns something



### Creating a custom front page

* call it front-page.php
* basis:

```php
<?php
genesis();
```


### Registering a widget area

Steps:

1. In `functions.php`, add the code that creates the widget area `genesis_register_sidebar( $array) );`

```php
genesis_register_sidebar( array(
    'id'        => 'page-widget',
    'name'        => __( 'Page Widget', 'nabm' ),
    'description'    => __( 'This is the widget area for a specific page.', 'nabm' ),
) );
```

2. In `front-page.php`, add the code that displays the contents of that widget area

```php
add_action('where', 'myFunction');
function myFunction() {
    genesis_widget_area('myId', array(before + after)
}

// Add the page widget in the content - HTML5
add_action( 'genesis_entry_footer', 'nabm_add_page_content' );
function nabm_add_page_content() {
    if ( is_page('ID') )
    genesis_widget_area ('page-widget', array(
        'before' => '<div class="page-widget"><div class="wrap">',
        'after' => '</div></div>',
    ) );
}
```


### Challenge: adding and displaying a widget

```php
genesis_register_sidebar( array(
    'id'        => 'my-widget',
    'name'      => __( 'My Widget', 'ramon' ),
    'description'   => __( 'This is the widget area for a specific page.', 'ramon' ),
) );

//* Add the page widget in the content - HTML5
add_action( 'genesis_entry_header', 'nabm_add_page_content' );
function nabm_add_page_content() {
    if ( is_single() )
    genesis_widget_area ('my-widget', array(
'before' => '<div class="page-widget"><div class="wrap">',
'after' => '</div></div>',
    ) );
}
```


_________________________

## WORKING WITH THE LOOP

### Digging deeper into the WordPress Loop

There are 2 ways to customize the WP loop

1. make some adjustments on the default query
    * exclude some categories
    * filter by author
    * order by name instead of date
    * etc.
2. create a whole custom query


For scenario 1:
-> use the pre_get_posts action

Exple:

```php
function exclude_category( $query ) {
    if ( $query->is_home() && $query->is_main_query() ) {
        $query->set( 'cat', '-1,-1347' );
    }
}
add_action( 'pre_get_posts', 'exclude_category' );
```

For scenario 2:

Typical usage when we need to run multiple loops in a same page
-> use the WP_Query object

```php
$the_query = new WP_Query( $args );
```

Genesis helps us with this with the `genesis_custom_loop()` function (in `lib/structure/loops.php`)


### Using a custom Genesis loop

The idea is to construct the $args array

We can use all these:  
https://www.billerickson.net/code/wp_query-arguments/




_________________________________________
____________________________________________

# WORDPRESS: BUILDING CHILD THEMES FROM SCRATCH

Recommended plugin:

* Genesis Visual Hook Guide plugin


______________________

## BUILDING A THEME

### Client-use vs Public-distribution

If you intend to distribute the theme, normally you will need to set up more theme or customization options than when for a single client

Here we will work a sample theme aimed at client-use (minimal options)


________________________

## SETTING UP YOUR BASIC THEME STRUCTURE

### Create your theme folder

In `wp-content/themes/scratch`  
Create a folder, the name is not important


### Create style.css

We need to create a stylesheet named style.css for the theme to work  
https://codex.wordpress.org/Theme_Development

Important fields:

* Theme name: this will appear in the Admin area
* Version: mahjor.nimor.bugs
* Tags: will complete in the end. It's not arbitrary
* Text dokmain: this is what's used for translation. cannot contain spaces
* Template: directory of the parent theme (genesis)

```php
/*
Theme Name: Twenty Thirteen
Theme URI: http://wordpress.org/themes/twentythirteen
Author: the WordPress team
Author URI: http://wordpress.org/
Description: The 2013 theme for WordPress takes us back to the blog, featuring a full range of post formats, each displayed beautifully in their own unique way. Design details abound, starting with a vibrant color scheme and matching header images, beautiful typography and icons, and a flexible layout that looks great on any device, big or small.
Version: 1.0
License: GNU General Public License v2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html
Tags: black, brown, orange, tan, white, yellow, light, one-column, two-columns, right-sidebar, flexible-width, custom-header, custom-menu, editor-style, featured-images, microformats, post-formats, rtl-language-support, sticky-post, translation-ready
Text Domain: twentythirteen

This theme, like WordPress, is licensed under the GPL.
Use it to make something cool, have fun, and share what you've learned with others.
*/
```

### Create functions.php

This file is used for many things, it can change the behaviour of our theme or of WP itself  
It acts kind of like a plugin within our theme, enabling us to hooks actions and filters in our theme, add theme support for various features, etc...  
https://codex.wordpress.org/Functions_File_Explained

We have to start with a doc header:

```php
<?php
/**
* Genesis Sample.
*
* This file adds functions to the Genesis Sample Theme.
*
* @package Genesis Sample
* @author  StudioPress
* @license GPL-2.0-or-later
* @link    https://www.studiopress.com/
*/
```

Then we have to initialize the Genesis framework. There are 2 ways

1. include `init.php`
```php
require_once get_template_directory() . '/lib/init.php';
```

=> go to the code to see what it does


2. preferred: hook into `init.php`

* loads the child theme before the parent
* this is standar WP behavior
* hook in functions before the Genesis framework is loaded

```php
do_action( 'genesis_setup' );
``` 



### Add a basic theme setup function

In `functions.php`:

```php
add_action( 'genesis_setup', 'scratch_setup' );
function scratch_setup() {
}
```


### Create front-page.php

Even though it's not required, most themes include it  
Some Genesis themes use home.php insetad. Don't:  
https://www.billerickson.net/dont-use-genesis-blog-template/

As every other template, it should include a call to genesis();



### Import demo content

When creating a theme, it's useful to import some dummy content, like from here:  
https://codex.wordpress.org/Theme_Unit_Test



### Challenge: create your basic theme structure

* create style.css with the template header
* create functions.php with the template header and load text domain and genesis_setup functions
* create fonrt-page.php with call to genesis()
* import demo content


_________________________

## GENERATING SITE FEATURES AND FUNCTIONALITY

### Add theme support options

First, we define some constants to refer to our child theme:

```php
// Defines the child theme (do not remove).
define( 'CHILD_THEME_NAME', 'Genesis Sample' );
define( 'CHILD_THEME_URL', 'https://www.studiopress.com/' );
define( 'CHILD_THEME_VERSION', '2.7.1' );
```

Then we start adding theme support for various features using the add_theme_support() function
https://developer.wordpress.org/reference/functions/add_theme_support/

By default, Genesis already add some feature in init.php

It doesn't include accessibility, viewport and html5 markup if there is a child theme, so we have to specifically include them in out child theme:

```php
// Adds support for HTML5 markup structure.
add_theme_support(
     'html5',
     array(
          'caption',
          'comment-form',
          'comment-list',
          'gallery',
          'search-form',
     )
);

// Adds support for accessibility.
add_theme_support(
     'genesis-accessibility',
     array(
          '404-page',
          'drop-down-menu',
          'headings',
          'search-form',
          'skip-links',
     )
);

// Adds viewport meta tag for mobile browsers.
add_theme_support(
     'genesis-responsive-viewport'
);
```

We also want to add support for footer widgets:

```php
// Adds support for 3-column footer widgets.
add_theme_support( 'genesis-footer-widgets', 3 );
```

More options:  
https://sridharkatakam.com/comprehensive-guide-genesis-theme-supports/



### Remove Genesis defaults

Genesis comes with a lot by default. If we want to remove something, we can

For example, unregister one of the 6 default layouts: `genesis_unregister_layout()`

https://carriedils.com/uncluttering-the-admin-experience/



### Register widget areas

Widget areas are useful to create a place in which users can drop in a widget

Sometimes, we'll just want to code it in the theme, other times we want to let users have a widget in there

We can use the genesis_register_sidebar function

```php
//Register the new sidebar
genesis_register_sidebar( array(
    'id' => ‘custom-sidebar’,//name this whatever makes sense
    'name' => ‘Custom Sidebar’,
    'description' => ‘This is a custom sidebar that we’re adding to Genesis’,
) );
```

If we have a lot of widget areas, it's better to put them in a separate file /includes/widget-areas.php and include it in functions.php



### Set up your front page to check out for widget areas

It is best practice to check first if there is content in the widget area with is_active_sidebar conditional

A good tip if we have a lot of widget areas is to create an array with all the conditionals. This kleeps cleaner


### Display active widget areas on your front page

To display a widget area:

```php
add_action( 'genesis_after_header', 'add_genesis_widget_area' );
function add_genesis_widget_area() {
                genesis_widget_area( 'custom-widget', array(
          'before' => '<div class="custom-widget widget-area">',
          'after'  => '</div>',
    ) );
}
```


________________

## BUILDING OUT YOUR CSS

Basically we go through the style.css sheet of the Genesis Sample Theme and do a lot of copy/paste

Overall:

* Add HTML5 reset and default elements
* Structure and layout
* Add Google Fonts
* Navigation
* Style custom widget areas
* Custom CSS



### Add HTML5 reset

copy/paste from Genesis Sample Theme



### Default HTML elements

She removes all the font-sizes in rem's
She says it's there for backwards compatibility


### Structure and layout

Start with higher level HTML element classes



### Navigation style

Section: Site Navigation



### Google fonts



### Add content to widget areas

She adds Simple Social Media Icons plugin



### Customize the site appearance

Add CSS, no real explanation


### Finish the Front page

Add CSS, no real explanation



______________________

## GOING FURTHER WITH CSS

### Media queries

Media queries are bits of CSS that enable to create a responsive website. We use breakpoints to determine how CSS applies depending on screen sizes


### Sass



________________________

## PUTTING IT ALL TOGETHER

### Prepare your theme

1. document your code
1. clean up the code
1. validate the code
1. test across platforms, devices and browsers
1. check for web accessibility


__________________________________

# MIGRATE WORDPRESS WITH WP MIGRATE DB

________________________________

## Introduction

### WP Migration in 3 steps

WordPress is a CMS that consists of a set of PHP files that interact with a database. All the content lies in the DB. The content and the application is completely separate.

The WP core is entirely replaceable. But these are not:
1. Themes
2. Plugins
3. Uploads
4. Database

WP migration consists of moving these 4 assets to a new location.

For files (1-3) it's easy, we just need to copy them to the new location via FTP or similar.

The tricky part is the database, because origin and destination may have different filesystems, all the URL in the database must be rewritten to match the destination. This is where plugins like WP Migrate DB come in place.

The migration is done in 3 steps:
1. Set up the target site (as brand new)
2. Migrate themes, plugins and uploads manually
3. Migrate the database


_________________________

## Using WP Migrate DB

### Move the necessary files with FTP

We create a new site with the **same table prefix in the DB**

We just need to copy the contents of `wp-content` folder.

This may take a while. After completed, we will see that all the themes and plugins are there. 

We don't need to activate plugins or themes, as this information is in the database, so they will be automatically activated once we migrate the DB

> Media files do not appear in WP backend so far. This is because Media objects are stored as posts in the DB, so they will appear once we migrate the DB


### Install WP Migrate on both sides

For the migration process to run smoothly, we need to install and activate the plugin on both origin and destination sites.


### The importance of matching table prefixes

We have to make sure that table prefixes in `wp-config.php` are the same in the destination site. 

> Apparently we can modify wp-config.php after intial installation, it doesn't seem to be a problem


### Export the origin database using WP Migrate DB

Using the free version of the plugin requires a 2-step process:
1. export the origin DB
2. import the DB into the detination site

We could do this directly in phpMyAdmin, but it's an error-prone process as we would have to mess with search/replace old URL's with new one. Plus we could break any serialized data.

WP Migrate DB does all this heavy lifting for us.

The plugin is installed under Tools/Migrate DB

Tab *Migrate*. Select:
* Save file in the computer (we need to upload it later)
* Compress as gzip (phpMyAdmin can upload .gzip)
* Find / Replace
    * Add if necessary https://old.com and http://new.com **after the first domain replacement**

> Here the trick is to install the plugin also in the destination server. That way when we log in to the plugin, we can just directly copy the local URL and path.

* Advanced Options. Check: 
    * Replace GUIDs
    * Exclude spam comments
    * Exclude transients

Click *Export* and obtain the .gzip file


### Import the database to the target site using phpMyAdmin

Now let's swith to the target site. In phpMyAdmin, navigate to the site's database.

The process is:
1. clear out the existing database
2. import the contents from the export file

To clear out:
1. go to *Structure* and then
2. Select *Check all*
3. select *Drop*

Now if we go to our target site, we should be redirected to the `install.php` page

Go back to phpMyAdmin
1. select Import tab
2. Browse -> select the .gzip
3. Click *go*

This should be it


### Other migration patterns

If we want to migrate one WWW site to another, we just need to:

1. Download files from WWW-1 to PC using FTP
2. Download database from WWW-1 to PC using WP Migrate
1. Upload files from WWW-1 to PC using FTP
2. Upload database from WWW-1 to PC using WP Migrate




______________________

## Common Problems and Solutions

### White screen of death

Most times, following a migration, the reason is that the theme is not available

To fix it, just access `./wp-admin`


### When the manual database import fails


### WP Migrate DB ate my posts


### Media files are not working


### The migration failed