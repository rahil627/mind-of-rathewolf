# conclusion
1. the python script is nearly perfect, for both parsing the body content and front mattter, just have to be careful of anything the markdown parser ate up. It also provides a config file to easily edit options. And, the script is so simple, you can edit it yourself (probably just have to change some options for html2text and markdownify libs it uses...).
2. the wordpress plugin is also really really good. You’d just have to get rid of some extra front matter (extra plugins), and use a markdown converter for things like links. Only extra newlines are lost. This method is special because it captures the final content, *after* it is processed by wordpress. So, if you’ve got a bunch of a plugins changing up the content, this is probably the way to go.
3. the jekyll-importer via xml was the worst, adding html tags everywhere, removing extra newlines, and preserving wayyy too much front-matter (meta seo plugins); but maybe useful to keep just for the sake of preservation of data, as a kinda last backup. After that, you’d have to throw it into a markdown parser and find some way to clean up the front matter (surely there’s a program for that...?). I'm not sure if it can be configured because jekyll’s docs are so sparse..


# body diff
## python script
  - converts html into text (via html2text python program) then
  - converts text into markdown (via markdownify? python program)
  - yet it **preserves all original new lines**
  - can possibly eat a few tags that were in the original post (for example: my `<cite>` is missing)
  - **provides options in the config file**, including a little spot to write replace text patterns
    - https://github.com/some-programs/exitwp/blob/master/config.yaml
  - the script says to run xmllint, but it didn’t make any changes for me. It might be for fixing xml errors... not sure

## the wordpress-plugin
  - **it preserves the content that was *displayed* by the post**. Unlike the python script which converts it into markdown, and unlike the ruby program which converts it into html, So, if there was any html in the original content of the post, it will show up here. If there wasn’t, it won’t add any either. It *preserves* the best.
    - the content, however, is the final content, processed through wordpress
    - this is better for the sake of preservation, as things can get eaten up by markdown converters (parsers?)
  - newlines are sorta *prettified*, like when you tell a text editor to clean / re-format your code, you know, consistently two newlines between everything
  
## jekyll-importer (via xml)
  - **converts content into html** (no matter what it originally was)
    - adds `<p>` and `<h>` everywhere (even if it wasn't in the original post!!)
    - converts single newlines into `<br />` where needed, which displays nicely in markdown... but using html
  - squashes all content, removing all of the vertical space :(

## jekyll-importer via database
  - todo


# front matter diff:
## python exitwp
  - **preserves what’s essential and names them nicely**, including the slug and complete link

## php(?) wordpress plugin
  - preserves a good amount of data, just excludes the “meta” plugins crap
  - preserves the original link name (baseurl/p=1343), which might be useful, in case of old links
  - removed the `/blog` in the permalink key (which is nice for me!)

## ruby jekyll-importer
  - preserves the most data including: published, status, *all* of the “meta” stuff including seo plugins
    - though, it’s probably good if you had special meta content, like page-specific meta `description`


# last update? / drafts
damn! turns out those three ways extracted a different amount of drafts: 5, ~30(?), and ~80. (the posts count were equal though)

the python script only caught 5, and uses the `published: false` tag, but it left them hiding in _posts folder. :( i had to use a `grep` ‘n `mv` script. :/

the wordpress plugin caught a lot more, probably the true drafts

jekyll’s own ruby program though caught the most, including various revisions and auto-saves...

so... just in case anyone ever does this, just try to finish those drafts before exporting! THEN can easily use that wordpress plugin or python script.


# tests
## FRONT MATTER

### python script:
```
---
author: rahil627
comments: true
date: 2013-09-19 10:24:09+00:00
layout: post
link: http://rahilpatel.com/blog/japanese-arcades/ #nice
slug: japanese-arcades #perfect!!
title: Japanese Arcades #perfect
wordpress_id: 2139
categories:
- Game Design
- Games
- Japan
- Thoughts
- Travel
---
```


### wordpress plugin:
```
id: 8034
title: Japan
date: 2016-11-30T09:12:30-05:00
author: rahil627
layout: post
guid: http://www.rahilpatel.com/blog/?p=8034 # maybe useful for referencing bad links?
permalink: /japan/ # good
medium_post: # can trash medium
  - 'O:11:"Medium_Post":11:{s:16:"author_image_url";s:74:"https://cdn-images-1.medium.com/fit/c/200/200/1*dmbNkD5D-u45r44go_cf0g.png";s:10:"author_url";s:28:"https://medium.com/@rahil627";s:11:"byline_name";N;s:12:"byline_email";N;s:10:"cross_link";s:2:"no";s:2:"id";s:12:"dfab5dd00bef";s:21:"follower_notification";s:3:"yes";s:7:"license";s:19:"all-rights-reserved";s:14:"publication_id";s:12:"7a04709b0155";s:6:"status";s:6:"public";s:3:"url";s:47:"https://medium.com/@rahil627/japan-dfab5dd00bef";}'
categories:
  - Action
  - Anthropology
  - Area
  - Art
  - Determinism and Free Will
  - Epistemology
  - Ethics
  - Experience
  - Experience
  - Humanities
  - Japan
  - Metaphysics
  - Personal
  - Philosophy
  - Political Economy
  - Political Philosophy
  - Rationalism
  - Rationality
  - Social Philosophy
  - Thoughts
  - Travel
---
```

### importer via xml:
```
---
layout: post
title: Japan
date: 2016-11-30 09:12:30.000000000 +00:00
type: post
parent_id: '0'
published: true # interesting, instead of having a drafts folder
password: ''
status: publish
categories:
- Action
- Anthropology
- Area
- Art
- Determinism and Free Will
- Epistemology
- Ethics
- Experience
- Humanities
- Japan
- Metaphysics
- Personal
- Philosophy
- Political Economy
- Political Philosophy
- Rationalism
- Rationality
- Social Philosophy
- Thoughts
- Travel
tags: [] # did i ever use this?
meta:
  medium_post: O:11:"Medium_Post":11:{s:16:"author_image_url";s:74:"https://cdn-images-1.medium.com/fit/c/200/200/1*dmbNkD5D-u45r44go_cf0g.png";s:10:"author_url";s:28:"https://medium.com/@rahil627";s:11:"byline_name";N;s:12:"byline_email";N;s:10:"cross_link";s:2:"no";s:2:"id";s:12:"dfab5dd00bef";s:21:"follower_notification";s:3:"yes";s:7:"license";s:19:"all-rights-reserved";s:14:"publication_id";s:12:"7a04709b0155";s:6:"status";s:6:"public";s:3:"url";s:47:"https://medium.com/@rahil627/japan-dfab5dd00bef";}
  _edit_last: '1'
  _yoast_wpseo_content_score: '30'
  _yoast_wpseo_primary_category: '207'
author:
  login: rahil627
  email: rahil627@gmail.com
  display_name: rahil627
  first_name: Rahil
  last_name: Patel
permalink: "/blog/japan/" # BAD
---
```








## CONTENTS

### official jekyll xml importer (wordpress.com importer)
```
<p>[exported from a markdown text file]<br />
[todo: still copying from notebook]<br />
[todo: need to fix #content blockquote p {<br />
    /* padding: 0px 0px 0px 0px; */<br />
}<br />
]</p>
<h2>Fuck Japan</h2>
<p>Fuck Japan.</p>
<p>That&#8217;s all I got.</p>
<p>Fuck Japan.</p>
<p>Perhaps the reason I never thought to talk to others when I lived in suburban America, anyone nearby, as I did during much of my 20s [and perhaps childhood], is because I simply wasn&#8217;t interested in the others. Japan [Japanese culture] has altered my behavior to not be interested in other people. As I [just earlier] peered through the express train&#8217;s window as it was rushing me toward the airport, perhaps the first time I&#8217;ve taken an express transport whilst having time, I didn&#8217;t care what is inside those buildings, those giant apartment complexes, the curtained shops, or traditionally-achitected homes.</p>
<p>Fuck &#8217;em.</p>
<h2>And here&#8217;s why</h2>
```






### plugin
```
[exported from a markdown text file]
[todo: still copying from notebook]
[todo: need to fix #content blockquote p {
    /* padding: 0px 0px 0px 0px; */
}
]

<h2>Fuck Japan</h2>

<p>Fuck Japan.</p>

<p>That&#8217;s all I got.</p>

<p>Fuck Japan.</p>

<p>Perhaps the reason I never thought to talk to others when I lived in suburban America, anyone nearby, as I did during much of my 20s [and perhaps childhood], is because I simply wasn&#8217;t interested in the others. Japan [Japanese culture] has altered my behavior to not be interested in other people. As I [just earlier] peered through the express train&#8217;s window as it was rushing me toward the airport, perhaps the first time I&#8217;ve taken an express transport whilst having time, I didn&#8217;t care what is inside those buildings, those giant apartment complexes, the curtained shops, or traditionally-achitected homes.</p>

<p>Fuck &#8217;em.</p>

<h2>And here&#8217;s why</h2>

<p>And here&#8217;s why:</p>
```





### python
```
[exported from a markdown text file]
[todo: still copying from notebook]
[todo: need to fix #content blockquote p {
    /* padding: 0px 0px 0px 0px; */
}
]

## Fuck Japan





Fuck Japan.





That's all I got.





Fuck Japan.





Perhaps the reason I never thought to talk to others when I lived in suburban America, anyone nearby, as I did during much of my 20s [and perhaps childhood], is because I simply wasn't interested in the others. Japan [Japanese culture] has altered my behavior to not be interested in other people. As I [just earlier] peered through the express train's window as it was rushing me toward the airport, perhaps the first time I've taken an express transport whilst having time, I didn't care what is inside those buildings, those giant apartment complexes, the curtained shops, or traditionally-achitected homes.





Fuck 'em.





## And here's why





And here's why:
```
