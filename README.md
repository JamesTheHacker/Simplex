Simplex
=======

Simplex is the easiest way to get up and running with PostCSS.

Instead of using Webpack, Gulp or any other build tool we use simple NPM scripts and commandline tools to create an easy to use CSS build tool.

Contains support for:

* [Autoprefixer](https://github.com/postcss/autoprefixer): Automatically adds vendor prefixes
* [CSSNext](http://cssnext.io): Use next generation CSS today
* [Lost Grids](https://github.com/peterramsing/lost): Create awesome grids
* [Rucksack](https://simplaio.github.io/rucksack/): CSS Superpowers
* [PostCSS Autoreset](https://github.com/maximkoretskiy/postcss-autoreset): Adds `all: initial` to all elements
* [CSSNano](http://cssnano.co/): Minify and optimize CSS

Usage
-----

Clone the repo:

    git clone https://github.com/JamesTheHacker/Simplex
    cd Simplex

Install packages:

    npm install

Now you can simply write your CSS as normal, save it under the `src` directory:

`src/post.css`

```css
.post {
  display: flex;
  background-image: linear-gradient(white, grey);
}
```

... and build:

    npm run build

This will output a single file called `css/main.css` in root directory:

```css
.post {
  display: -webkit-box;
  display: flex;
  background-image: -webkit-linear-gradient(white, grey);
  background-image: linear-gradient(white, grey);
}
```

Minify
------

Simplex can minify and optimize your CSS using [cssnano]:

    npm run minify

This will output a minified CSS file and store it under `css/main.min.css`. If you encounter a duplication warning during minification you can safely ignore it.

Watch
-----

PostCSS can automatically recompile your CSS whenever you save a file. Run the following command:

    npm run watch


Browser Targeting
-----------------

Autoprefixer allows you to target specific browsers. For example you can target all modern browsers including the last 2 versions, or the top 5%, or whatever you like. See [Browserlist](https://github.com/ai/browserslist) for more information.

Currently I've set it to the `last 2 versions`. To change simply modify `config.json`. Specifically the following line:

    "autoprefixer": {
        "browsers": "last 2 versions"
    }
