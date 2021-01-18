---
title: "Hugo Static Site Generator Directory Structure Explained"
date: 2021-01-18T08:12:18-05:00
draft: false
---

## Directory Structure Explained

The following is a high-level overview of each of the directories with  links to each of their respective sections within the Hugo docs.

- [`archetypes`](https://gohugo.io/content-management/archetypes/)

  You can create new content files in Hugo using the `hugo new` command. By default, Hugo will create new content files with at least `date`, `title` (inferred from the file name), and `draft = true`. This saves time and promotes consistency for sites using multiple content types. You can create your own [archetypes](https://gohugo.io/content-management/archetypes/) with custom preconfigured front matter fields as well.

- [`assets`](https://gohugo.io/hugo-pipes/introduction/#asset-directory)

  Stores all the files which need be processed by [Hugo Pipes](https://gohugo.io/hugo-pipes/). Only the files whose `.Permalink` or `.RelPermalink` are used will be published to the `public` directory. Note: assets directory is not created by default.

- [`config`](https://gohugo.io/getting-started/configuration/)

  Hugo ships with a large number of [configuration directives](https://gohugo.io/getting-started/configuration/#all-variables-yaml). The [config directory](https://gohugo.io/getting-started/configuration/#configuration-directory) is where those directives are stored as JSON, YAML, or TOML files.  Every root setting object can stand as its own file and structured by  environments. Projects with minimal settings and no need for environment awareness can use a single `config.toml` file at its root.

Many sites may need little to no configuration, but Hugo ships with a large number of [configuration directives](https://gohugo.io/getting-started/configuration/#all-variables-yaml) for more granular directions on how you want Hugo to build your website. Note: config directory is not created by default.

- [`content`](https://gohugo.io/content-management/organization/)

  All content for your website will live inside this directory. Each top-level folder in Hugo is considered a [content section](https://gohugo.io/content-management/sections/). For example, if your site has three main sections—`blog`, `articles`, and `tutorials`—you will have three directories at `content/blog`, `content/articles`, and `content/tutorials`. Hugo uses sections to assign default [content types](https://gohugo.io/content-management/types/).

- [`data`](https://gohugo.io/templates/data-templates/)

  This directory is used to store configuration files that can be used by Hugo when generating your website. You can write these files in  YAML, JSON, or TOML format. In addition to the files you add to this  folder, you can also create [data templates](https://gohugo.io/templates/data-templates/) that pull from dynamic content.

- [`layouts`](https://gohugo.io/templates/)

  Stores templates in the form of `.html` files that specify how views of your content will be rendered into a static website. Templates include [list pages](https://gohugo.io/templates/list/), your [homepage](https://gohugo.io/templates/homepage/), [taxonomy templates](https://gohugo.io/templates/taxonomy-templates/), [partials](https://gohugo.io/templates/partials/), [single page templates](https://gohugo.io/templates/single-page-templates/), and more.

- [`static`](https://gohugo.io/content-management/static-files/)

  Stores all the static content: images, CSS, JavaScript, etc. When Hugo builds  your site, all assets inside your static directory are copied over  as-is. A good example of using the `static` folder is for [verifying site ownership on Google Search Console](https://support.google.com/analytics/answer/1142414?hl=en), where you want Hugo to copy over a complete HTML file without modifying its content.

From **Hugo 0.31** you can have multiple static directories.

- resources

  Caches some files to speed up generation. Can be also used by template authors to distribute built SASS files, so you don’t have to have the  preprocessor installed. Note: resources directory is not created by  default.

##