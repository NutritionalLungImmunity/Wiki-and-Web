# Wiki-and-Web
Wiki and web pages for the aspergillus simulation project

This repository contains a wiki and associated web pages in support of the aspergillus simulation projects.

This project is currently a NIH funded U01 (related grants include U01 EB024501). Team members include UConn Health, UF Health, and Kitware. The purpose of the work is to computationally simulate the invasion of the human lungs by by spores of the aspergillus fungus. The project is inherently multiscale with interconnected cell level, organ level (alveoli ducts), and organ level (lungs) models.

The project is being developed to ensure reproducible science. All data, software tools, and methods will become publicly available as they are developed. As these data and methods are being created by different groups, the wiki and web pages in this repository serve as high-level organizational guide to various resources. These resources include software (simulation and visualization), genomics data, simulation data, associated metadata, experimental lab notebooks, and presentation materials.

For questions please contact the project PI Dr. Reinhard Laubenbacher @ UConn Health (laubenbacher "at" uchc.edu).

# For developers
The website is now using the [Bulma Clean Theme](http://www.csrhymes.com/bulma-clean-theme/) ([GitHub](https://github.com/chrisrhymes/bulma-clean-theme))

## Getting Started
To get the site running locally on your machine...

#### Step 1:
Clone this repository

#### Step 2:
You'll need to make sure your `Gemfile` looks something like this:
```
# frozen_string_literal: true

source "https://rubygems.org"

git_source(:github) {|repo_name| "https://github.com/#{repo_name}" }

# gem "rails"

gem "bulma-clean-theme"

gem 'github-pages', group: :jekyll_plugins
```

#### Step 3:
Once you've updated your `Gemfile`, open a terminal and navigate to your site's root and type `bundle update`.

This will recompile everything needed to build the site.

#### Step 4:
That's pretty much it. You can now run `bundle exec jekyll serve` like you would normally to build the site and preview at `localhost:4000` or `127.0.0.1:4000`
