# About

This example shows one way to use Typescript and Angular 2 in a
monolithic Rails 5 application *without* using the asset pipeline.

The Angular 2 app lives in the ng-app folder. ng-app/\*.ts is compiled
to public/\*.js using tsc -w via npm start. See package.json for
details.

There are two systemjs.config.js files. The one in the root folder is
used by tsc to compile \*.ts files. The one in the public folder is used
at run time by the browser to load \*.js files. Using this pattern, we
could theoretically have a separate systemjs.config.js per Rails view
to load separate Angular 2 apps per Rails view.

The nice thing about this example is that it doesn't use webpack, gulp,
or any other weirdness. This is straight Rails 5 and Angular 2.

# Installation

* bundle install

* gem install foreman

* npm install

# If the typings directory doesn't exist after npm install:

* npm run typings install


# Starting the server and compiling the typescript to js

* foreman start

* visit http://localhost:5100/ in a browser to see the angular 2 page
