# medinLaVie.github.io

Github Workplace is pretty cool.

Okay, now I just have to find the right jekyll templates.
https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll


====== begain:jekyll wiki ======
## How to add a page?
Say, if you want to add /about /projects /contact. How do you do that?
https://jekyllrb.com/docs/pages/
- add an HTML file
- add a markdown file

```
.
├── about.md    # => http://example.com/about.html
├── index.html    # => http://example.com/
└── contact.html  # => http://example.com/contact.html
```

## How to add a post
You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

Jekyll requires blog post files to be named according to the following format:

`YEAR-MONTH-DAY-title.MARKUP`

Where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit numbers, and `MARKUP` is the file extension representing the format used in the file. After that, include the necessary front matter. Take a look at the source for this post to get an idea about how it works.

### Add Images and PDFs

... which is shown in the screenshot below:
![My helpful screenshot](/assets/screenshot.jpg)
... you can [get the PDF](/assets/mydoc.pdf) directly.

### Add Code
Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

## Test site locally
https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll#building-your-site-locally

1. `bundle install`
2. `bundle exec jekyll serve`
```
$ bundle exec jekyll serve
> Configuration file: /Users/octocat/my-site/_config.yml
>            Source: /Users/octocat/my-site
>       Destination: /Users/octocat/my-site/_site
> Incremental build: disabled. Enable with --incremental
>      Generating...
>                    done in 0.309 seconds.
> Auto-regeneration: enabled for '/Users/octocat/my-site'
> Configuration file: /Users/octocat/my-site/_config.yml
>    Server address: http://127.0.0.1:4000/
>  Server running... press ctrl-c to stop.
```

3. To preview your site, in your web browser, navigate to `http://localhost:4000`.

==== end:jekyll wiki ====

==== begin:liquid syntax ====
## Liquid 101
https://shopify.github.io/liquid/basics/introduction/

## Objects
`Objects` contain the content that Liquid displays on a page.
- Objects and variables are displayed when enclosed in double curly braces: {{ and }}.

`Tags` create the logic and control flow for templates.
- The curly brace percentage delimiters {% and %} and the text that they surround do not produce any visible output when the template is rendered.
- This lets you assign variables and create conditions or loops without showing any of the Liquid logic on the page.

`Template` tags tell Liquid where to disable processing for comments or non-Liquid markup,
- and how to establish relations among template files.


```liquid
<!-- output -->
{{ page.title }}

<!-- control flow -->
{% if user %}
  Hello {{ user.name }}!
{% endif %}

<!-- iteration -->
{% for product in collection.products %}
  {{ product.title }}
{% endfor %}

<!-- template -->
{% assign verb = "turned" %}
{% comment %}
{% assign verb = "converted" %}
{% endcomment %}
Anything you put between {% comment %} and {% endcomment %} tags
is {{ verb }} into a comment.

```

=== font ===
https://fonts.google.com/


=== SCSS ===
https://sass-lang.com/guide/#preprocessing

=== jekyll themes ===
[A clean and minimalist theme for Jekyll](https://news.ycombinator.com/item?id=20806300)
https://github.com/joway/hugo-theme-yinyang?tab=readme-ov-file

=== jekyll minima theme ===
This is the base Jekyll theme. You can find out more info about customizing your Jekyll theme, as well as basic Jekyll usage documentation at [jekyllrb.com](https://jekyllrb.com/)

You can find the source code for Minima at GitHub:
[jekyll][jekyll-organization] /
[minima](https://github.com/jekyll/minima)

You can find the source code for Jekyll at GitHub:
[jekyll][jekyll-organization] /
[jekyll](https://github.com/jekyll/jekyll)


[jekyll-organization]: https://github.com/jekyll

=== jekyll resource and talks ===
Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/

=== alternatives to jekyll ===
[Blog]
https://jekyllrb.com/
https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll
https://www.gatsbyjs.com/showcase/

https://docusaurus.io/showcase

[Documentation]
https://docusaurus.io/docs/next

[Gatsby]
- https://docusaurus.io/docs/next#gatsby
- https://www.gatsbyjs.com/starters/

[Supabase](https://supabase.com/blog/chatgpt-supabase-docs)

[docs]
https://stripe.com/newsroom/news/bfcm2023
