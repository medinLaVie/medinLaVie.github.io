# medinLaVie.github.io

`rvm install ruby` has been stuck on my laptop for 5m+. I gave up. I'm going to use github workplace as it seems more convenient. 

I meant to check out the github workplace more often, as an alternative. Yay! both ruby/gem/jekyll up-to-date versions were already installed. 

It takes only 1 min to setup the workplace, and I'm ready to code. 

Github Workplace is pretty cool. (at least, I found the experience pleasant so far.)

Pros: 
- agnostic to the local compute resource.
- perfect to write a blog / fix a bug on the personal site.  


Cons: 
- requires good network 


Okay, now I just have to find the right jekyll templates. 

https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll


# How to add a page? 
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

# Test site locally
https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll#building-your-site-locally

1. bundle install
2. 
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


