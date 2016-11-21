---
layout: post
title:  "Sticky footer layout"
date:   2016-11-18 15:29:36 +0100
categories: jekyll css html
---

The default layout used with Jekyll places the footer right after the
page content. This looks quite okay until you change the background color of
the footer. Then it becomes obvious that the footer is right after the content
and then there is a blank space if the header, content and footer are not enough
to fill the whole screen. This doesn't look so nice.

## Creating sticky footer using flexbox in CSS

In my solution, which I am using on this website, I used flexbox.
To implement this I had to examine the html file `_layouts/default.html`
in the root folder or my Jekyll blog. I had to create a CSS stylesheet file
and had to link it to the head of the pages.

### Creating and linking a CSS stylesheet to your Jekyll blog

1. I created a file, `default.css` in the `css` directory.
2. Opened `_includes/head.html` and added the following line inside the `<head>`
    tag underneath the link for `/css/main.css`

    {% highlight html %}
<link rel="stylesheet" href="{{ '{{ "/css/main.css" | prepend: site.baseurl ' }}}}">
<!-- The link bellow is the new one that has to be added to the file -->
<link rel="stylesheet" href="{{ '{{ "/css/default.css" | prepend: site.baseurl ' }}}}">
    {% endhighlight %}

### Checking html files to find the classes we need for the CSS rules

The starting point for the layout of all of the pages on a Jekyll site is
`_layouts/default.html` file. So let's examine its contents:

{% highlight html %}
<!DOCTYPE html>
<html>

  {{ "{% include head.html " }}%}

  <body>

    {{ "{% include header.html " }}%}

    <div class="page-content">
      <div class="wrapper">
        {{ "{{ content " }}}}
      </div>
    </div>

    {{ "{% include footer.html " }}%}

  </body>

</html>
{% endhighlight %}

We can see that inside the `<body>` there is a `<div>` of **page-content** class
that holds all the content that will be loaded from the html or md file.
The footer itself is loaded from `footer.html.`

### Creating flexbox layout
Open up `/css/default.css` and the following content:
{% highlight css %}
body {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
.page-content {
    flex: 1;
}
{% endhighlight %}

Save the file and reload your page.
Now the footer will stick to the bottom of the page.

### Why did this work

First we created a flexbox container, which was the whole `<body>` by writing
`display: flex;`.
Then we specified that we want to order the items inside the container
bellow each other by `flex-direction: column;`.
Then we said that the flexbox container should be as tall as
the viewpoint (browser window) by `min-height: 100vh;`.

And finally, we specified **page-content** as the only flex item, so that all of the free space is used only by this element.
