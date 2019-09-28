# php-autoload-hello-world

Create directory named `php-autoload-hello-world`


Files Structure
We can put all files inside the main dir, but recommended way is to create another dir, as `src` to be easier to understand and maintain our code organized. The project structure will start with the follow: `php-autoload-hello-world/src/HelloWorld/`

We will create our classes inside "HelloWorld" directory.

Now we need to have `composer.json` file. For that we need to go inside our project's root directory using terminal. Then run `composer init` and answer simple questions. It will create `composer.json`

Add some configuration in `composer.json`

```
"require": {
    "php": "^7.1.2"
},
"autoload": {
    "psr-4": {
        "HelloWorld\\": "src/HelloWorld/"
    }
}
```

Now, run `composer install` inside root directory. It will create `vendor` directory and `composer.lock` file inside root directory.

To test our working code, create `tests/test.php` file inside root directory and call any class method that we have created inside `src/HelloWorld` directory.


#### Uploading code at GitHub

Create repository named `php-autoload-hello-world` at github. And run following commands inside our project root directory.

```
git init
git remote add origin git@github.com:usmanakram/php-autoload-hello-world.git
git add --all
git commit -m "initial files"
git tag -a v1.0.0 -m "initial release"
git push -u origin master
```

