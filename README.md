# react-npm-component-starter

## Synopsis

A starter kit for publishing small and efficient react components to NPM and http://react-components.com/.


## Features

* [React](http://facebook.github.io/react/), of course.
* [Webpack](http://webpack.github.io/) for asset bundling.
* [React hot loader](https://github.com/gaearon/react-hot-loader) enabled out of the box. Changes to React components will show in the browser immediately without a full reload.
* [Babel](https://babeljs.io/) for ES6+ transpilation.
* [SASS](http://sass-lang.com/) (SCSS or Sass style) and [Autoprefixer](https://github.com/postcss/autoprefixer) enabled by default through Webpack.
* Image loaders setup and ready to go so you can reference your images as `require()` statements in JS, or just use `url()` as usual in CSS and Webpack will take care of the rest.
* Production configuration with best practices applied for optimizing React file size.
* [ESLint](http://eslint.org/) Support for ESLint via babel-eslint.

This kit is intentionally missing a specific Flux implementation, or any other non-essential library, as I use this as a base for experimenting with various parts of the React ecosystem.


### Directory Layout

```
.
├── /build/                     # The folder for compiled output
├── /__test__/                  # Jest Test Intigration 
├── /node_modules/              # 3rd-party libraries and utilities
├── /view/                      # Use to test and view the react component
│   ├── /styles/                # Global styles
│   ├── /entry.jsx              # React Entry
│   ├── /template.html          # index.html template
├── /component/                 # React Component 
│   ├── /index.jsx              # Component JSX file
│   └── /webpack.config.js      # Component styling file
└── package.json                # The list of 3rd party libraries and utilities
```


## In the wild

* [React Upload Button](https://github.com/Deepblue129/upload-button)
* [React Color Panel](https://github.com/Deepblue129/color-panel)
* [React Birds](https://github.com/Deepblue129/react-birds)


## Usage

Fork this repo, then run:

```
npm install
npm start
```

That will fire up a webpack dev server in **hot** mode. Most changes will be reflected in the browser automatically without a browser reload. You can view the app in the browser at `http://localhost:8080`.

## Building

To generate a production build, run:

```
npm run build
```

The above command will generate a `build` folder with the appropriate component.js file along with the minified CSS and JS files. 
This can be directly published to NPM via:

```
npm publish
```

## Modifying the HTML

The HTML file is generated using the `view/template.html` file. This file is used for both the development build.


## License

MIT