# Static site pages for NIH Commons demo
This repository contains a minimal Jekyll framework for a DERIVA demo. It includes a homepage, link into chaise, About page, Privacy Policy page and Contact page.

## Prequisites

You should have jekyll installed locally in order to run "jekyll serve" and review the site locally. Jekyll is a Ruby Gem and requires Ruby. Note that you will need at least 

- [Installation Guide](https://jekyllrb.com/docs/installation/)

The quick version:

Before you start, make sure your system has the following:

- Ruby version 2.2.5 or above, including all development headers (ruby installation can be checked by running ```ruby -v```)
- RubyGems (which you can check by running ```gem -v```)
- GCC and Make (in case your system doesn’t have them installed, which you can check by running ```gcc -v```,```g++ -v``` and ```make -v``` in your system’s command line interface)

Run ```gem install bundler jekyll```

## Configuring

Update the following Markdown and Yaml files:

- Homepage: `index.md` 
- Navigation: `_data/nav.yml`
- About page: `about/index.md`
- Privacy Policy: `privacy-policy/index.md` - This is boilerplate content. But review to make sure it reflects the demo.
- Contact page: `contact/index.md'

To update the branding (using image or text in upper left corner of the navbar):

- Using text as brand: 
    - `_includes/navbar.html`: go to the line `<span id="brand-text">Demo Name</span>` and update the Demo Name.
    - `/assets/css/custom.css`: Make sure the first two rules are commented out.
- Using image as brand: 
    - Image should be 50px high or less.
    - Add your logo file to `/assets/img/`
    - `/assets/css/custom.css`: Make sure the first two rules are NOT commented out and update `background: url(/assets/img/deriva-h50-simple.png) no-repeat;` with path to logo file. You might need to adjust css styles.
    
## Reviewing locally

Go to the root of the repository and run `jekyll serve`. You'll be able to see the generated HTML at `http://127.0.0.1:4000/`.

## Deploying site

We're still figuring out the best way to go.

A few options:
- Run `jekyll serve` or `jekyll build` to build your site into the `_site/` directory of your repo. Then rsync this to the `/var/www/html/` directory of the intended server. 
    - Note that the `.gitignore` file prevents the `_site/` directory from being added to the repo.  
- Copy the jekyll framework into a /www/ subdirectory of the project/demo repo.
    - Add recipes similar to the facebase recipes and makefile/scripts
- Fork the jekyll framework to a new repo `<demo-name>-www`
    - Add recipes similar to the rbk recipes and makefile/scripts

