# generator-wordpress-themify

A modular Wordpress theme generator for [Yeoman](http://yeoman.io).
Mostly based on popular [Roots](https://github.com/roots/roots) starter theme, plus inspiration from the mighty generator-webapp.

(Still in early stage, please use with caution! See the [TODO](https://github.com/Chmood/generator-wordpress-themify/blob/master/TODO.md) to see what's going on.)


## Features

* Bootstrap, in Less, Sass or plain css version
* Modernizr (with custom optimized build) 
* CSS autoprefixer
* Image minification
* True 'dist' folder for production theme
* Unit testing with Mocha
* Coffeescript (and Coffeelint)
* Some sample example files

All features are optional, take only what you need!


## Quick start


### Tools installation

> WARNING : by now, this generator hasn't been registered on npm yet. Just clone this repo, and ```npm link``` inside its directory. Will be fixed soon!

(Assuming you already have node and yo installed properly)

Install Themify globally (it requires having admin rights) :

```
npm install -g generator-wordpress-themify
```


### Theme creation

Browse to your wordpress theme folder. Something like :

```
cd /var/www/wordpress/wp-content/themes/
```

Create a directory, name it something like 'dev' or 'mytheme-factory', no matter, and jump into it :

```
mkdir dev && cd $_
```

Install your theme and configure options :

```
yo wordpress-themify
```

Build your dev theme, and start watching for file change

```
grunt serve
```

### Theme activation

In the Wordpress admin pannel, go to Appearance > Themes. Activate the development version of your theme. Browse to your site, and eventually turn on your browser's livereload plugin now.

When using unit-tests, you can also open a tab on http://127.0.0.1:9001 where tests report will be live-reloaded


### Workflow

Now you're all set up, start building a great theme!
```grunt serve``` will watch for any source file modification, process them if needed, and refresh your browser

In case you don't use ```grunt serve```, you can compile your dev theme manually :

```
grunt app
```

Once you're done, build an optimized production theme :
(You can set the destination folder in Gruntfile.js)

```
grunt dist
```
(You can also just use ```grunt```, the default task.)


And then switch wordpress to use this production theme.
(But do keep a copy of the development files!)


Have fun!



## License

[MIT License](http://en.wikipedia.org/wiki/MIT_License)
