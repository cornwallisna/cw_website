---
layout: content_page
---

{% if false %}

WARNING: Many of the highlighted links directly on this page will not work if you are viewing this page directly in Github. Instead,
you can see the complete page [here](https://fcassirer.github.io/cw_website/README/index.html) which will be fully expanded by Jekyll and the links are in working order.

{% endif %}

# Cornwallis Neighborhood Association (CNA) Website

This website uses Jekyll and the Responsive Starter Template to provide a website for the Cornwallis Neighborhood Community.  The goal of the website is to provide a live newsletter such that information can be shared more quickly and at less cost than our quarterly newsletter.

# Features

* Simple home page for important news
* Running blog entries for use by board members
* Showcase some community pictures via google albums
* Membership signup and renewal instructions
* Association by-laws and document archive
* Support for our communitY sponsors
* Website feedback and issue tickets

# How it works

Authorized members of the CNA team can submit updates to this Github repository and upon approval the website is recreated and published.  The overall structure of the website is anticipated to be somewhat static with various pre-defined pages being updated by the CNA.  The following pages can be edited as follows:

* [home page]({{site.github_url}}/blob/pending/index.md) - Front page [edit]({{site.github_url}}/edit/pending/index.md)
* [news page]({{site.github_url}}/blob/pending/news.md) - News page [edit]({{site.github_url}}/edit/pending/news.md)
* [presidents page]({{site.github_url}}/blob/pending/presidents.md) - Presidents Message page [edit]({{site.github_url}}/edit/pending/presidents.md)
* [vicepresidents page]({{site.github_url}}/blob/pending/vicepresidents.md) - Vice Presidents Message  page [edit]({{site.github_url}}/edit/pending/vicepresidents.md)
* [aboutus page]({{site.github_url}}/blob/pending/aboutus.md) - About page [edit]({{site.github_url}}/edit/pending/aboutus.md)
* [membership page]({{site.github_url}}/blob/pending/membership.md) - Membership/Enrollment page [edit]({{site.github_url}}/edit/pending/membership.md)
* [blogs page]({{site.github_url}}/blob/pending/blogs.md) - Blog entries page, note, you probably don't need to edit this [edit]({{site.github_url}}/edit/pending/blogs.md)

## Jekyll and frontmatter

[Jekyll](https://jekyll.com) is a framework used by Github to easily define and manage web pages.  This site is a combination of Jekyll and the [Simple Responsive Template](http://www.prowebdesign.ro/simple-responsive-template/conditions-use.html) which provides the web site layout.

Frontmatter is a [Jekyll](https://jekyllrb.com/docs/front-matter/) term that refers to some configuration information that can be added to the top of a Jekyll page.

### Supported frontmatter for this site

|name | description | layout type |
|:----------|-------------|-------------|
|layout | The type of template page, i.e, home, content_page, article | all |
|topnav| the name(s) of the menu items to highlight when on this page| all |
|banner| Something interesting to say at the top of a page| all |
|image: feature: | name of a png, jpg etc image file to be used above any text.| all |
|image: teaser: | name of a png, jpg etc image file to be used on the blog listing page| article |
|sponsors| Position or disable advertisement banners.  "off" will disable on the page, other options are "top" or "bottom"| all |
|title| Title of the page or article | all |
|modified| Date and Time of the form YYYY-MM-DD<b>T</b>HH:MM:SS<b>-04:00</b>.  Note the text in <b>bold</b> is required as is.  Example, 2021-01-26T11:30:41-04:00 is Jan 26, 2021 at 11:30:41am EDT (-04:00 timezone) |
|tags| Keywords for future search| all |

### Images

Images are jpg, png, or any other supported picture type.  Typically, they are stored in the images/ folder.  The 'image:' frontmatter tag assumes any image name unless otherwise specified is found in the images/ folder.   For example, <b>garage-sale.png</b> would be [{{site.github_url}}images]({{site.github_url}}/tree/pending/images).  Images can also be links to pictures on the web by providing the URL instead of the image/ link.

Images can be added to the repository via [drag and drop]({{site.github_url}}/upload/pending/images) or by clicking on the Add Files button

## Adding a new blog entry

New blog entries are created in the [_posts folder]({{site.github_url}}/blob/pending/_posts) folder.  These files are named as YYYY-MM-DD-anythingyouwant.md.  For example, 2021-02-02-groundhogsday-update.md where you could tell everyone where to see the groundhogs.

Each blog entry is a Jekyll article page.  An example article might look like:

<pre>
---
layout: article
title: "Garage sales!!!!!"
categories: articles
modified: 2021-01-26T11:30:41-04:00
tags: general,garagesale
sponsors: "bottom"
image:
  feature: garage-sale.png
  teaser: https://bit.ly/3tiPl6k
---

## This is a header

This is content, we are having a garage sale ...

</pre>

You can [create a new blog entry]({{site.github_url}}/new/pending/_posts) directly.  Simply cut and paste the above frontmatter into the new file and add your text below the `---`.  Be sure to change the image to suit your blog entry (See above for how to upload a new image).

## Advertising

There is a fairly simple advertising capability that will put a scrolling picture slider at the top, side, or bottom of a page.  The contents of the advertising window is controlled by a list of advertiser pictures and captions.

This file can be found in the _data/sponsors.yml file.  To add or remove advertisers simply edit [this file]({{site.github_url}}/blob/pending/_data/sponsors.yml).
The file is made of of a list of 4 values:

* img: is the name of the image, usually found in images/ads/
* caption: Text caption about the sponsor, maybe a phone number of website link etc.
* link: Some kind of link that clicking the picture will take you to.  It could be a sponsors website, a mailto: or tel: type link if they do not have a website.
* name: The name of the advertisor

For example:

<pre>
slides:
  - img: /images/ads/DesignsToAT.png
    caption: Designs To A "T", <a href="tel:239-549-5995">239-549-5995</a>
    link: mailto:designs2aT@comcast.net
    name: DesignsToAT
</pre>

The order that these entries are listed is the order they are displayed on the website.

# Original README from Simple Responsive Starter Template

Simple is a responsive starter web site template. It is intended to be basic and bare-bone, with minimum styling and options included. Still, it has features clients usually would ask for: menu with drop-downs, slider, grid layout. See full list of features below.

Simple is mainly for web designers (beginner to intermediate level). But it is so simple (pun intended:) ), that any person with very little knowledge of HTML can modify and use it.

To build a website with Simple, download it and add your own content and pages. Or, if you want a different design, you can tweak the CSS. In either case, you will have a device-agnostic website that works and looks great on smart phones, tablets, laptops, and desktops. This tutorial will get you started and help you build a fully-functional site.

Simple is compatible with FireFox, Google Chrome, Opera, Opera Mini, Safari, IE9, 10. It is also compatible with IE8, but they will see the mobile layout. IE 6 and IE7 Must Die!

Simple is a FREE software, released without any warranty under Common Public Attribution License. Simple can be used in personal or commercial projects for free provided you keep the attribution statement intact. Read more about terms of use here http://www.prowebdesign.ro/simple-responsive-template/conditions-use.html

If you want to use Simple without attribution link, buy us a coffee and get a waiver: http://www.prowebdesign.ro/simple-responsive-template/conditions-use.html
