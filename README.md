# deriva-tutorial-www

This repository contains the jekyll framework for static site pages of the DERIVA Tutorial Sandbox server.

## Prequisites

You should have jekyll installed locally in order to run "jekyll serve" and review the site locally. Jekyll is a Ruby Gem and requires Ruby. Note that you will need at least

- [Installation Guide](https://jekyllrb.com/docs/installation/)

The quick version:

Before you start, make sure your system has the following:

- Ruby version 2.2.5 or above, including all development headers (ruby installation can be checked by running ```ruby -v```)
- RubyGems (which you can check by running ```gem -v```)
- GCC and Make (in case your system doesn’t have them installed, which you can check by running ```gcc -v```,```g++ -v``` and ```make -v``` in your system’s command line interface)

Run ```gem install bundler jekyll```

## Jekyll framework

The following are the main files to generate the site:

- `_config.yml` - Uses "name" and "description" fields for Browser title and site description
- `index.md` - This is the homepage.
- `privacy-policy/index.html` - This is boilerplate content. But review to make sure it reflects the demo.

To change the branding (using image or text in upper left corner of the navbar):

- Using text as brand:
    - `_includes/navbar.html`: go to the line `<span id="brand-text">Demo Name</span>` and update the Demo Name.
    - `/assets/css/custom.css`: Make sure the first two rules are commented out.
- Using image as brand:
    - Image should be 50px high or less.
    - Add your logo file to `/assets/img/`
    - `/assets/css/custom.css`: Make sure the first two rules are NOT commented out and update `background: url(/assets/img/deriva-h50-simple.png) no-repeat;` with path to logo file. You might need to adjust css styles.

## Reviewing locally

Go to the root of your forked repository and run `jekyll serve`. You'll be able to see the generated HTML at `http://127.0.0.1:4000/`.
