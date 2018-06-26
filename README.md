# deriva-web-template

This repository contains a minimal Jekyll framework for a DERIVA demo static site to use with DERIVA demos and as the starting part of deployment static sites. It includes a homepage, link into chaise, About page, Privacy Policy page and Contact page.

## Fork this repo

Do not clone this repo. Fork it instead and then when we make improvements, you can update from master.

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

Update the following files:

- `\_config.yml` - Update "name" and "description"
- `index.html` - This is the homepage. Edit to include the name of the project/demo and at least a one line description. Include any specific links into Chaise that would be useful.
- `about/index.html` - You can update the suggested content in there as necessary. But add at more description of the project/demo than is on the homepage and ideally include a related image.
- `privacy-policy/index.html` - This is boilerplate content. But review to make sure it reflects the demo.

To update the branding (using image or text in upper left corner of the navbar):

- Use text as brand: 
    - `\_includes/navbar.html`: go to the line `<span id="brand-text">Demo Name</span>` and update the Demo Name.
    - `/assets/css/custom.css`: Make sure the first two rules are commented out.
- Use image as brand: Image should be 50px high or less.
    - Add your logo file to `/assets/img/`
    - `/assets/css/custom.css`: Make sure the first two rules are NOT commented out and update `background: url(/assets/img/deriva-h50-simple.png) no-repeat;` with path to logo file.
    
## Reviewing locally

Go to the root of your forked repository and run `jekyll serve`. You'll be able to see the generated HTML at `http://127.0.0.1:4000/`.

## Deploying site

We're still figuring out best way to go.

A few options:
- Run 'jekyll serve' or 'jekyll build' to build your site into the `\_site/` directory of your repo. Then rsync this to the /var/www/html/ directory of the intended server. 
- Copy the jekyll framework into a /www/ subdirectory of the project/demo repo.
    - Add recipes similar to the facebase recipes and makefile/scripts
- Fork the jekyll framework to a new repo `<demo-name>-www`
    - Add recipes similar to the rbk recipes and makefile/scripts

I'll flesh out what those last two recipes/makefiles/scripts should look like.