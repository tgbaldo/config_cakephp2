# config_cakephp2
Passo a passo para configurar a aplicação CakePHP 2.x

## composer.json
{
  "name": "my_app",
  "require": {
    "cakephp/cakephp": "2.8.*"
  },
  "config": {
    "vendor-dir": "Vendor/"
  }
}

## criando um projeto
Vendor/bin/cake bake project .

## configurando o bootstrap com autoload do composer
// Load Composer autoload.
require APP . 'Vendor/autoload.php';

// Remove and re-prepend CakePHP's autoloader as Composer thinks it is the
// most important.
// See: http://goo.gl/kKVJO7
spl_autoload_unregister(array('App', 'load'));
spl_autoload_register(array('App', 'load'), true, true);
