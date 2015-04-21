# Magento Hello World exemple plugin.
## what it is
This is an example tutorial repository that explains how to create a plugin for magento.

As it grows in features it is split into different branches.

## What it does


* [step 1](https://github.com/tinyapps-br/magento-hello-world-extension/tree/step-1)
  * Routes to a controller
    * Responds to:

```
  /helloworld?name=yourname
  /helloworld/index/goodbye?name=yourname
```

* [step 2](https://github.com/tinyapps-br/magento-hello-world-extension/tree/step-2)
  * The previous index action renders a custom block
  * The previous goodbye action renders a different layout

## Installation via composer
Add the required repositories to the composer.json of your Magento project.
```
"repositories": {
    "magento-hello-world-extension": {
        "type": "vcs",
        "url": "git@github.com:elvetemedve/magento-hello-world-extension.git"
    },
    "magento-version-checker": {
        "type": "vcs",
        "url": "git@github.com:elvetemedve/MagentoVersionChecker.git"
    }
}
```

Add the module package as dependency to the project.
`composer require "inviqa/magento-hello-world-extension:114.*"`


### Package version conventions
Composer package versions are represented as GIT tags.

A tag combined is a combination of two the Magento version and the module version.
Let's suppose we have Magento EE 1.14.2 and module version 1.2.3, then the combined tag version will be
114.1.2.3. This allows us to have the latest version of the module which is compatible with the Magento version
used by the project. So a `composer update` is enough to upgrade all Magento modules at once. 

### Known issues

You may get the error below when running composer install the first time.
```
[ErrorException]                                                                                                  
  include(MagentoHackathon\Composer\Magento\Deploystrategy\.php): failed to open stream: No such file or directory
```
Workaround: run `composer install` again.

## Author
Marcelo Jacobus

## Kudos
* Alan Storm for [this tutorial](http://alanstorm.com/magento_controller_hello_world).
* Manish Prakash [for this tutorial serie](http://www.excellencemagentoblog.com/magento-blogs/module-development-series/)