---
id: directory-structure
---

## Directory structure

The root of your project should include a `composer.json` file. All dependency management should be handled through [composer](https://getcomposer.org).

* `src/`: All PHP code goes here
* `public/`: Use this directory for web applications (sites, apis, etc), it should include:
    * `index.php`: This file simply includes ../app/bootstrap.php and starts the app
    * `.htaccess`: Use the template
* `app/`: Put the application code in. This directory should include:
    * bootstrap.php (includes vendor/autoloader.php, and instantiates services)
    * schema.xml Database schema if applicable. It should be compatible with `dbtk/schema-loader`
* `config/`: Contains the application config files:
    * `services.yaml`: Application specific configuration
    * `routes.yaml`: A file defining all the routes (for symfony/routing)
    Other configuration can go in `config/` too if needed.
* `examples/`: Any example PHP code or example data files (xml, json, etc)
* For Silex apps, put the application code in src/Application.php (extends Silex\Application)
