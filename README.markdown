# My Blog

My blog using [Octopress.org](http://octopress.org/docs) powered by [Jekyll](https://github.com/mojombo/jekyll).

Embed code (with [Solarized](http://ethanschoonover.com/solarized) styling) in your posts from gists, jsFiddle or from your filesystem.

# Usage Notes

## Command line

```bash
# create a new post
rake new_post['Title of the post']

# create a new page 
rake new_page['Title of the page']

# preview your work
rake preview

# publish it
rake generate && rake deploy

# commit and backup(automatic message)
git commit -am "`date`" && git push origin source
```

## Creating a post

You can create a post just by adding a .markdown file in the source/_posts folder and preview it with `rake preview`. The name of the file will be your post url so use an appropriate [slugified name][1].

You must add some metas at the top of the file :

```
---
layout: post
title: My Awesome article.
date: 2013-05-1 00:00
categories: news technology web
author: Super Man
comments: true
published: false
---
```

If you set `published: false`, your posts will only be visible in preview mode.


## Publish

When ready, just use `rake generate && rake deploy` to publish it :)

# License
(The MIT License)

Copyright © 2009-2013 Brandon Mathis

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the ‘Software’), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED ‘AS IS’, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.


# If you want to be awesome.
- Proudly display the 'Powered by Octopress' credit in the footer.
- Add your site to the Wiki so we can watch the community grow.
