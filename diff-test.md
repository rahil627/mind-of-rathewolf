
there was no difference between the linted xml (using xmllint) and original xml import, using the exitwp.py script

in general:
the python script is the best, content only, no html, perfect front matter, only problem is that it destroyed the newlines
  - uses htmltotxt python program; maybe can check how that handles <br>?
  - edit the config file, at the end, there's a spot for replace expressions
    - https://github.com/some-programs/exitwp/blob/master/config.yaml
the jekyll-importer (via xml) correctly adds <br /> where needed
the wordpress-plugin, although is html, still messes up the newlines?


front matter diff:
jekyll-importer adds '/blog' to the permalink :(
wordpress plugin stores the original link name, which might be useful

jekyll-importer has more data: published, status, tags
  - check if i ever used tags


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

