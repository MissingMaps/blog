### Adding Blog Posts

Blog post are added to the [missingmaps](http://missingmaps.org) site by adding a new file here.

Images go in the `arcmaps/share/blog-pictures/` S3 bucket, should be named following `missingmaps-blog_YYYYMMDD_my-file-name.extension`, and should be resized to an appropriately small size. Banner images should have the hue/saturation reduced.

Copy an early blog post as a template. Follow the image file naming conventions and talk to us about putting the image files in the same AWS S3 bucket as all the other images (talk to daniel.joseph@redcross.org if you need support).

First create a file with the following naming conventions YYYY-MM-DD-[title-of-post].md For instance the first blog post is named 2016-05-05-intro-to-missing-maps.md

Next add the following to the top of your new file. This 'front matter' is important for the page meta data and so that it will build correctly.

````
---
layout: post
title: [title of your post]
postID: [unique-post-id]
category: [category]
banner: [url of banner image]
date: YYYY-MM-DD
author: [author]
excerpt: [excerpt from your post]
published: true
tags: [tag1, tag2]
permalink: /blog/:year/:month/:day/:title/
lang: en
---
````

#### Sample front matter

````
---
layout: post
title: Missing Maps
postID: missing-maps
category: blog
banner: https://arcmaps.s3.amazonaws.com/share/blog-pictures/missingmaps-blog_20160422_banner.jpg
date: 2016-05-05
author: Dale Kunce
excerpt: Welcome to the new Missing Maps Blog. Over nearly the last two years you almost 10,000 mappers have contributed over 22 million edits, almost 3 million buildings and 300,000 km of roads. These achievements are truly amazing. The new blog will focus on sharing some of the personal stories and major events happening with Missing Maps.
published: true
tags: [Partners, Project update]
permalink: /blog/:year/:month/:day/:title/
lang: en
---
````
