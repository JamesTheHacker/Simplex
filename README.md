PostCSS Autoprefixer Boilerplate
================================

This is a simple boilerplate template to quickly get up and running with PostCSS Autoprefixer. It uses npm scripts to prefix, bundle and build all your CSS files into a single file.

Now you can write plain old CSS and never have to worry about browser prefixes.

Usage
-----

Clone the repo:

    git clone https://github.com/JamesTheHacker/PostCSS-Autoprefixer-Boilerplate
    cd PostCSS-Boilerplate

Install packages:

    npm install

Now you can simply write your CSS as normal, save it under the `css` directory:

**css/post.css**

    .post {
        display: flex;
        background-image: linear-gradient(white, grey);
    }

... and build:

    npm run build

This will output a single file called `main.css` in the `build` directory with prefixes:

    .post {
        display: -webkit-box;
        display: flex;
        background-image: -webkit-linear-gradient(white, grey);
        background-image: linear-gradient(white, grey);
    }


Seriously, it's that simple. You never need write a browser prefix in your life!
