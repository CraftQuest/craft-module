# Craft Module
A started Craft CMS module for learning how to extend Craft CMS using [CraftQuest.io](https://craftquest.io) tutorials.

## Installation

1. Download the module as a zip file.
2. Unzip and place the `craft-modules` directory in your `modules` directory in the Craft CMS project.
3. Update your Craft CMS project's `config/app.php` file to include the module and bootstrap it.
```php
   return [
    'id' => App::env('APP_ID') ?: 'CraftCMS',
    'modules' => [
        'craft-module' => craftquest\CraftModule::class,
    ],
    'bootstrap' => ['craft-module'],
]; 
```
4.  Update the project's `composer.json` file to add the module to the `autoload` section of the file. It should look something like this:
```php
     "autoload": {
    "psr-4": {
      "craftquest\\": "modules/craft-module/src"
    }
  }, 
```

5. Rebuild the project's Composer autoload files: `composer dump-autoload` 
