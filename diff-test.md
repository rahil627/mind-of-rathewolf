


# conclusion
1. the python script is nearly perfect, for both parsing the body content and front mattter, just have to be careful of anything the markdown parser ate up. It also provides a config file. And, the script is so simple, you can edit it yourself (probably just have to change some flags for html2text and markdownify...).
2. the wordpress plugin is really good, but would still have to get rid of some extra front matter. Only extra newlines are lost.
3. the jekyll-importer via xml was the worst, adding html tags, removing extra newlines, though adding breaklines correctly in case of single newlines, and preserving way too much front-matter; but good to keep for the sake of preservation of data. I'm not sure if it can be configured...


# body diff
python script
  - converts html into text (via html2text) then
  - converts text into markdown (via markdownify?)
  - yet it **preserves all original new lines** (although, they will not display corectly in markdown)
  - can possibly eat a few tags that were in the original post (my `<cite>` is missing)
  - **provides options in the config file**, including a little spot to replace patterns
    - https://github.com/some-programs/exitwp/blob/master/config.yaml
  - xmllint changed nothing for me


# jekyll-importer (via xml)
  - **converts content into html** (no matter what it originally was)
  - adds `<p>` and `<h>` everywhere (even if it wasn't in the original post!!)
  - correctly converts single newlines into `<br />` where needed, which displays nicely in markdwon
  - squashes all content, removing all of the vertical space

# jekyll-importer via database
  - todo


# the wordpress-plugin
  - **no html, but it preserves html that was originally in the post**
  - **generally preserves newlines, but removes them if there's more than 3 newlines**, like "prettiying" code
  - doesn't convert text into markdown, so the links are still in html







# front matter diff:
python exitwp
  - **preserves whats essential and names them nicely**, including the slug and complete link

ruby jekyll-importer
  - preserves the most data including: published, status, *all* of the `meta` stuff

php(?))wordpress plugin
  - preserves a good amount of data, just excludes the meta crap
  - preserves the original link name (p=1343), which might be useful, in case of old links
  - removed the `/blog` in the permalink key (which is nice for me!)


#### import

##### python script:
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



##### wordpress plugin:
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


##### importer via xml:
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









#CONTENTS

## official jekyll xml importer (wordpress.com importer)
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







## plugin
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






# python
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

