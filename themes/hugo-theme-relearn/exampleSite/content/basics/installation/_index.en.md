+++
tags = ["documentation"]
title = "Installation"
weight = 15
+++

The following steps are here to help you initialize your new website. If you don't know Hugo at all, we strongly suggest you learn more about it by following this [great documentation for beginners](https://gohugo.io/overview/quickstart/).

## Create your project

Hugo provides a `new` command to create a new website.

```
hugo new site <new_project>
```

## Install the theme

Install the Relearn theme by following [this documentation](https://gohugo.io/hugo-modules/use-modules/#use-a-module-for-a-theme) using Hugo's module system.

This theme's repository is: https://github.com/McShelby/hugo-theme-relearn.git

Alternatively, you can [download the theme as .zip](https://github.com/McShelby/hugo-theme-relearn/archive/main.zip) file and extract it in the `themes` directory

### From Git

If you install the theme from your git repository or GitHub, you have several options.

If you use the `head` of the `main` branch, you are using the development version. Usually it is fully functional but can break from time to time. We try to fix newly introduced bugs in this version as soon as possible.

Additionally you can checkout one of the tagged versions. These tagged versions correspond to an official [releases from the GitHub repository](https://github.com/McShelby/hugo-theme-relearn/releases).

Besides the usual version tags (eg `1.2.3`) there are also tags for the main version (eg. `1.2.x`), major version (eg. `1.x`) and the latest (just `x`) released version making it easier for you to pin the theme to a certain version.

## Basic configuration

When building the website, you can set a theme by using `--theme` option. However, we suggest you modify the configuration file `hugo.toml` and set the theme as the default. You can also add the `[outputs]` section to enable the [search functionality](basics/customization#activate-search).

{{< multiconfig file=hugo >}}
theme = "hugo-theme-relearn"
[outputs]
home = [ "html", "rss", "search", "searchpage"]
{{< /multiconfig >}}

## Create your first chapter page

Chapters are pages that contain other child pages. It has a special layout style and usually just contains a _chapter name_, the _title_ and a _brief abstract_ of the section.

````md
### Chapter 1

# Basics

Discover what this Hugo theme is all about and the core concepts behind it.
````

renders as

![A Chapter](chapter.png?width=60pc)

The Relearn theme provides archetypes to create skeletons for your website. Begin by creating your first chapter page with the following command

````shell
hugo new --kind chapter basics/_index.md
````

By opening the given file, you should see the property `chapter=true` on top, meaning this page is a _chapter_.

By default all chapters and pages are created as a draft. If you want to render these pages, remove the property `draft: true` from the metadata.

## Create your first content pages

Then, create content pages inside the previously created chapter. Here are two ways to create content in the chapter:

````shell
hugo new basics/first-content.md
hugo new basics/second-content/_index.md
````

Feel free to edit those files by adding some sample content and replacing the `title` value in the beginning of the files.

## Launching the website locally

Launch by using the following command:

````shell
hugo serve
````

Go to `http://localhost:1313`

You should notice three things:

1. You have a left-side **Basics** menu, containing two submenus with names equal to the `title` properties in the previously created files.
2. The home page explains how to customize it by following the instructions.
3. When you run `hugo serve`, when the contents of the files change, the page automatically refreshes with the changes. Neat!

## Build the website

When your site is ready to deploy, run the following command:

````shell
hugo
````

A `public` folder will be generated, containing all static content and assets for your website. It can now be deployed on any web server.

{{% notice note %}}
This website can be automatically published and hosted with [Netlify](https://www.netlify.com/) (Read more about [Automated HUGO deployments with Netlify](https://www.netlify.com/blog/2015/07/30/hosting-hugo-on-netlifyinsanely-fast-deploys/)). Alternatively, you can use [GitHub pages](https://gohugo.io/hosting-and-deployment/hosting-on-github/).
{{% /notice %}}