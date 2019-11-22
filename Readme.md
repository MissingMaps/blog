### Adding Blog Posts

Blog posts are added to the [Missing Maps site](http://missingmaps.org) by adding a new file here. Click on the Create new file botton on top of this page and a new file will open.

First name your file with the following naming conventions YYYY-MM-DD-[title-of-post].md For instance the first blog post is named 2016-05-05-intro-to-missing-maps.md

Next copy and paste the following to the top of your new file. This 'front matter' is important for the page meta data and so that it will build correctly.


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

You will need to adapt everything between the square brackets. See below for an example. 

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

After having adapted the font matter, start writing your blogpost.

To format the text you will need to use Markdown. Find [here](https://guides.github.com/features/mastering-markdown/) a guide. You could also check out how other blog posts look like. 

The images of your article should be named following `missingmaps-blog_YYYYMMDD_my-file-name.extension`, and should be resized to an appropriately small size. Banner images should have the hue/saturation reduced. 

Images go in the `arcmaps/share/blog-pictures/` S3 bucket. Talk to us about putting the image files in the same AWS S3 bucket as all the other images (talk to daniel.joseph@redcross.org).

Once your images are in teh AWS S3 bucket, you will have to add a link to the image into your text. Use the below formatting for this. 

````
 <figure>
<img src="https://arcmaps.s3.amazonaws.com/share/blog-pictures/missingmaps-blog_YYYYMMDD_my-file-name.extension">
<p class="caption">write here the caption of your image</p>
</figure>
````
 See below an example. 
 
 #### Sample figure

````
 <figure>
<img src="https://arcmaps.s3.amazonaws.com/share/blog-pictures/missingmaps-blog_20191001_screenshot-new-project-types.png">
<p class="caption">Two new project types are available in MapSwipe 2.0</p>
</figure>
````

Once all the edits are done, click Commit new file. The file will be reviewd by one of the administrators and will be added on the blog page of the Missing Maps website.  
