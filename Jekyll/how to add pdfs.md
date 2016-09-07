# How to add pdfs to your static website

I followed [Jameson Zimmer's advice](http://jamesonzimmer.com/simple-pdf-embed-for-jekyll/):

Simply upload a pdf for example via Google Docs. Then, insert an iframe to a markdown page:

```html
---
title: "Creation of a Landscape: The Logic or Urbanization in the PRC"
description: NYU East Asian Studies Department, MA Thesis Defense
date: 2013-11-01
layout: pdf
categories: writing
permalink: /writing/creation-of-a-landscape/
---

<iframe src="https://docs.google.com/file/d/0B8aGkJVsdqiJamVpUnJ1TDlFbFU/preview" width="100%" height="100%"></iframe>
```

In case you want to create blank markdown pages, create a new layout:

```html
<
<!DOCTYPE html>
<html>
  <body>
    {{ content }}
  </body>
</html>
```

And [this is how it looks like](https://moxpower.github.io/cv/).
