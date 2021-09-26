
This repository is the source code of [Linping's website](https://yuanlinping.top).
I created this website mainly based on [Dominik Moritz's](https://github.com/domoritz/domoritz.github.io) template, with some modifications borrowed from my labmates [Shelly](https://shellywhen.github.io/) and [Haotian](https://haotian-li.com/). It was written with [Jekyll](https://jekyllrb.com/). 

Like my website? Go through the following three steps to create your own website!

## Step 1: Run this repository on your computer
1. Clone this repository to your computer.
2. Follow the [official instruction](https://jekyllrb.com/docs/installation/) to install Jekyll and its dependencies.
3. Go to the root directory and run the code with the following command in the terminal.
  ```
  bundle exec jekyll build
  bundle exec jekyll serve
  ```
`gem install` or `bundle install` may be needed to install other dependencies.
If running successfully, you can open localhost:4000 to visit the website.

## Step 2: Modify the content
### Jekyll tutorial
Go through the [official tutorial](https://jekyllrb.com/docs/step-by-step/01-setup/) to learn the usage of Jekyll and this [article](https://www.taniarascia.com/make-a-static-website-with-jekyll/) to understand its common file structure.

### File structure in this repo
```
root directory
|   _config.yml
|   style.scss
|   index.md
|   publications.md
|   projects.md
|   cv.html
|   _layouts/
|   _sass/
|   _includes/
|   _data/
|   _publication/
|   assets/
|   images/
|   _site/
```
- `_config.yml` is the configuration file. We can define variables here, which can be accessed globally by {{site.variable_name}}.
- `style.scss` defines gloable variables to control styles. It also imports .scss from `_layouts/`. 
- `index.md`, `publications.md`, `publications.md` are the entries.
Their [front matter](https://jekyllrb.com/docs/front-matter/) indicates its layout and class, which control the layout and styles of a webpage, respectively. The `layout` property links to corresponding files in `_layouts/`, and the `class` property links to corresponding files in `_sass/`.
- `_includes/` contains files that show up on every page, such as header and footer. It also contains files that implement the complex layout, interaction, and content. To import the files in `_includes/` to other files, using `{% include xx.html xx1=xx1%}`.
- `_data/` and  `_publication/` stores data referred in other files. Using `site.data.file_name` to gbet the data.
- `assets/`  and `images/` are assets.
- `_site/` is automatically generated. No need to edit it.

### How to update the content 
If the current template meets all your needs, what you need to do to create your website is simple.
1. Change my personal information to your information. They are mainly in the following files: `_config.yml`, `index.md`, `_includes/footer.html`, `_includes/head.html`, and `cv.html`.
2. Modify or update files in `_data/` and add assets to `assets/`.

### How to modify the template
You can modify the template to meet your needs.
- Change layouts or styles: go to the `_layouts/` and `_sass/` folder.
- Add a new tab in addition to `Publications`, `Projects`, and `CV`: add a new .md file in the root directory. You may also need to add corresponding files in `_layouts/`, `_sass/`, `_includes/`, and `_data/`.


## Step 3: Host your webstie in Github pages
- [official documentation](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll)
- [a simple tutorial](https://idratherbewriting.com/documentation-theme-jekyll/mydoc_publishing_github_pages.html)