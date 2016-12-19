# Angular Skeleton Configuration #

## Install Seed ##

> Install Seed from here [angular2-webpack-starter](https://github.com/AngularClass/angular2-webpack-starter)

## Install PrimeNg, Font-Awesome, jquery and Bootstrap ##

> npm install primeng - -save
> npm install font-awesome - -save
> npm install jquery - -save
> npm install bootstrap@3 - -save

## Add dependency ##

Add this into app.component.ts styleUrls
> `'../../node_modules/primeng/resources/themes/omega/theme.css',
    '../../node_modules/primeng/resources/primeng.min.css',
    '../../node_modules/font-awesome/css/font-awesome.min.css',
    '../../node_modules/bootstrap/dist/css/bootstrap.min.css',`

Add loader for font in webpack.common.js
> `{ test: /.(woff(2)?|eot|ttf|svg)(\?[a-z0-9=\.]+)?$/,loader:'url-loader?limit=100000' }`

Provide new plugin for jquery in webpack.common.js

> `new webpack.ProvidePlugin({
        jQuery: 'jquery',
        $: 'jquery',
        jquery: 'jquery'
      }),`

Import dependency in vendor.browser.ts
> `import 'jquery/dist/jquery.min.js';
	import '../node_modules/bootstrap/dist/js/bootstrap.min.js';`
