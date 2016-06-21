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
