# Journal Theme

This is the theme used for Journal. It's a heavily modified fork of the fantastic [Casper theme.](https://github.com/vjeantet/hugo-theme-casper).

## Features

Here are just some of the features offered by this theme (you can find a [live demo](https://duo-labs.github.io/journal/post/team/jwright/features/) in our documentation which is itself an instance of Journal):

* Tagging
* Pagination
* Syntax Highlighting
* Support for multiple authors
* Google Docs embedding
* Warnings, notes (and sidenotes!), and tips
* LaTEX support (through KaTEX)
* Diagrams from MermaidJS
* Client-side searching
* Table-of-contents and hoverable anchor links

This theme also includes the following optional (disabled by default) services:

* Google Analytics (optional - disabled by default)
* Disqus (optional - disabled by default)
* Share buttons on Facebook, Twitter, Google (optional - disabled by default)

# Theme usage and asumptions

* All blog posts are in the `post` folder (`content/post`)
* All authors are in the `authors` folder (`content/authors`)
* All datasets are in the `datasets` folder (`content/datasets`)

# Installation

## Installing this theme

It's recommended to use this theme as part of a Journal instance. However, you can use this theme as a standard Hugo theme:

```
mkdir themes
cd themes
git clone https://github.com/duo-labs/journal-theme journal-theme
```

# Configuration

The configuration for this theme can be found in `config.toml`. Here is an example configuration:

``` toml
baseURL = "https://your_site_here"
languageCode = "en-us"
title = "Labs Journal"
enableEmoji = true
pygmentsCodeFences = true
pygmentsStyle = "lovelace"
theme = "journal-theme"
assetDir = "themes/journal-theme/static/"
[params]
    logo = "/images/Duo-Labs-Logo.svg"
    share = false
[taxonomies]
  author = "authors"
  category = "categories"
  tag = "tags"
  dataset = "datasets"
[outputs]
  home = [ "HTML", "JSON", "RSS" ]
```

## Example Metadata For Each Post

``` yaml
---
title: Open Sourcing Journal - How Labs Keeps Notes
authors:
- jwright
tags:
- opensource
- journal
draft: true
date: 2019-08-12T21:25:43
---

Everything above the "more" tag will be rendered in the list preview.
<!-- more -->
You can have the rest of the content here.
```

More information can be found in our [Journal documentation](https://duo-labs.github.io/journal).
