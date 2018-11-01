# Portfolio Website

## Quick Start
```
# 1 Clone this repo
# 2 Navigate into the repo directory
# 3 Install all node packages
npm install
# 4 Get started
gulp serve - starts localhost server with browser-sync, watches HTML, Sass, JS with hot reloading
gulp - minify CSS/JS and builds your app into the dist directory, ready for production
```

## Gulp commands


```
gulp serve
```

**gulp (build)**

```
gulp
```

**gulp concatScripts**

The gulp concatScripts command combines the specified JS resources into main.js
You can add new JS files to this command on line 16 in gulpfile.js
You might want to run concatScripts once separately after adding new JS files.
```
gulp concatScripts
```

## Overwriting Bootstrap sass variables
You can overwrite specific bootstrap sass variables by uncommenting lines in assets/css/1-frameworks/bootstrap/bootstrap-user-variables.scss

## PHP
If you need a server with PHP support you can use the project with [MAMP Pro](https://www.mamp.info/en/mamp-pro/) or similar.
* Create a new host in the hosts panel of MAMP Pro and choose the project folder as the document root.
* Enable Symlinks settings in the "Extended" tab of the host configuration.
* On line 82 in gulpfile.js change the browserSync.init function to the following:
```
browserSync.init({
    proxy: "http://name-of-your-mamp-host:8888",
    open: "external"
});
```
* Start the MAMP services and run "gulp serve" as before.
