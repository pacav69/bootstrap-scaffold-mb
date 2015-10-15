Bootstrap-Scaffold-modern-business
============
[![Built with Grunt](https://cdn.gruntjs.com/builtwith.png)](http://gruntjs.com/)
![build](https://travis-ci.org/pacav69/bootstrap-scaffold-mb.svg?branch=master)

> Bootstrap Scaffold - Modern Business by SilverPC.
Based on a template from [startbootstrap](http://startbootstrap.com/template-overviews/modern-business/) 

## Setup

- Download the zip package
- Create a working directory
- extract files from the zip file into the working directory
- open up a command prompt in the working directory
- type the following:


	`npm install`

this will read the package.json and do a preinstall

	"scripts": {
	    "preinstall": "npm install -g grunt-cli bower jshint",
	    "prestart": "npm install",
	    "postinstall": "bower install",
	    "start": "grunt serve",
	    "test": "grunt test"

## Alternate method of setup
## Getting Started
_If you haven't used [grunt][] before, be sure to check out the [Grunt Getting Started][] guide._

### Grunt

Install grunt-cli globally:

```
npm -g install grunt-cli
```


[grunt]: http://gruntjs.com
[Grunt Getting Started]: http://gruntjs.com/getting-started

### Bower

*If you haven't used [bower][] before, be sure to check out the [Bower Getting Started][] guide.*

Install bower globally then use bower install to install `bower_components` as listed in bower.json into the directory app/bower_components as directed by the contents of .bowerrc file

	{
	    "directory": "app/bower_components"
	}


```
npm -g install bower
```

```
bower install
```


[bower]: http://bower.io/
[Bower Getting Started]: http://bower.io/#getting-started

### Other files

Install the rest of nodejs files. 

```
npm install
```

## Grunt server

use grunt server:

```
grunt server
```

Build all files.

```
grunt
```

## Usage

## Using bower_components in html files

### For example using CSS files

    <!-- build:css({.tmp,app}) css/main.css -->
    <link rel="stylesheet" type="text/css" href="bower_components/bootstrap/dist/css/bootstrap.min.css"/>

    <link rel="stylesheet" href="bower_components/mediaelement/build/mediaelementplayer.min.css"/>
    <link href="styles/style.css" rel="stylesheet">
    <!-- endbuild -->

### For example using Javascript files

    <!-- build:js({.tmp,app}) js/scripts.js -->
    <script src="js/main.js"></script>
    <!-- endbuild -->


	<!-- build:js js/plugins.js -->
    <script type="text/javascript" src="bower_components/fastclick/lib/fastclick.js"></script>
    <script src="http://code.jquery.com/jquery-2.0.3.min.js"></script>
    <script type="text/javascript">
    /*<![CDATA[*/
    window.jQuery || document.write('<script type="text/javascript" src="bower_components/jquery/jquery.min.js"><\/script>');
    /*]]>*/
    </script>

    <script src="bower_components/mediaelement/build/mediaelement-and-player.min.js"></script>
    <script src="bower_components/bootstrap/dist/js/bootstrap.min.js"></script>
    <script type="text/javascript" src="bower_components/gmaps/gmaps.js"></script>
    <!-- endbuild -->

## Alternative options
Using another bootstrap template

- Visit the site [startbootstrap](http://startbootstrap.com "startbootstrap")
- Select a template and download the file
- Delete the app contents except the bower_components directory
- extract the files from the downloaded file
- copy the files into the app directory

### Concatenate files
If you want to concatenate CSS files then surround them with

    <!-- build:css({.tmp,app}) css/[sample].css -->
		{your css files list}
	<!-- endbuild -->
    
for example:

	<!-- build:css({.tmp,app}) css/main.css -->
		<link rel="stylesheet" type="text/css" href="bower_components/bootstrap/dist/css/bootstrap.min.css"/>
		<link href="styles/style.css" rel="stylesheet">
	<!-- endbuild -->

This will create a css/main.css in the dist folder when the build option is selected using grunt build or grunt and inserts into the html files as one file. 


	<link rel="stylesheet" href="css/main.css">

   
If you want to concatenate js files then surround them with 

	<!-- build:js js/scripts.js -->
		{your js files list}
	<!-- endbuild -->
for example:

	<!-- build:js js/scripts.js -->
	<script src="bower_components/mediaelement/build/mediaelement-and-player.min.js"></script>
    <script src="bower_components/bootstrap/dist/js/bootstrap.min.js"></script>
	<!-- endbuild -->
This will create a js/scripts.js in the dist folder when the build option is selected using grunt build or grunt and inserts into the html files as one file. 


	<<script src="js/scripts.js"></script>


### References
[startbootstrap templates](http://startbootstrap.com "startbootstrap")

[placehold images](http://placehold.it/ "placehold images")
