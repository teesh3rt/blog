---
title: the migration to jekyll
description: ...was actually quite easy!
date: 2025-10-28T12:42:24+02:00
icon: (OvO)
tags: [blog, development]
featured: true
draft: false
---

today, i decided to migrate the site to jekyll for easing the process of managing this blog. honestly, it improved my workflow a lot, and the templating language is very nice.

## extensibility and minimalism

when i first started using it, i thought using a theme was mandatory: that every jekyll site required a theme in order to work, and if you wanted to make your site your own, you needed to make your theme and publish it as a gem. as it turns out, no!

jekyll is actually very very extensible, and also very very minimal, which is a rare thing to see nowadays! if you want, you can ditch the theme system (and most systems, in fact) entirely: here is the entire configuration file for this blog as of now

```yaml
title: teeshs terminal
description: >-
  a blog about everything, run by teesh3rt
baseurl: ""
```

very very minimal, very very nice :D

## ease of creation: content is king

before the migration, i needed to make sure that the pages were up to date with `posts.json`. this is no longer a neccesity! jekyll bundles content and metadata together into one file, which is in the markdown format (very nice!).

a file might look something like this:

```yaml
---
title: my awesome blog post
description: its awesome trust me
icon: (V_V) # you dont just have to stick to a schema!
tags: blog personal
layout: post
---

hello! this is my post.
```

i also no longer have to make sure that each post is up to spec with a layout! jekyll has layout files via the `_layouts` directory so that i dont ever need to worry about those.

## who needs react?

jekyll also has supports for **includes** where react has components. if you want to reuse a certain template, not for a whole page but for a simple part of it, you can just make an include file!

you can even pass parameters via the `include` variable provided automatically for you!
