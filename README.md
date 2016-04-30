## Ideas

An open source list of half-baked ideas.  Anyone is free to take these ideas
and run with them.

#### Twitter audio client:

An account owner has an option to speak a string of words. Then people can just
listen to their tweets being spoken aloud in their voice.  If an account owner
hasn't uploaded an audio sample then there could just be a default voice that
the end user chooses.

As a user, instead of constantly checking twitter, you could just listen to
speak in realtime while you work.  It would probably be pretty weird.

Media could be introduced and autoplayed.

#### Discrete CSS diff

This idea has a few possible uses

* Everytime someone tries to check in some css, they get instant feedback to
  let them know if they aren't introducing any new visual styles (rules) to the
  codebase.  A list of classes referencing the same visual styles could be
  returned to promote reuse within a codebase.

* Site checker. You could compare two different sites and get back and object
  that contained all of the unique css for each codebase in regards to rules
  (property value pairs).

* Could compare the top 1000 sites on alexa and show the list of unique css
  amongst all of them vs the css that each site contains.


#### Navigation Visualizer

You could scrape websites and grab all links in the header and footer of each
website.  Could check for elements and id or classnames that are equal to a set
of common names to denote nav: navbar, nav-bar, nav, site-links, etc.

Build a data visualization that shows common patterns in website navigation.
i.e 80%  of sites use store, 20% use shop.  Things to potentially visualize:
  * Whether links are in header or footer
  * Order of links
  * Text used for page names

Could divide visualizations by types of site, i.e e-commerce, news, startup,
personal portfolio.

#### Automated component documentation

First grab all links for a given site. Could use something like: ``` wget
--spider --force-html -r -l2 $url 2>&1 \ | grep '^--' | awk '{ print $3 }' \ |
grep -v '\.\(css\|js\|png\|gif\|jpg\)$' \
  > urls.txt
```

For each view generate an [ast from the dom](https://github.com/iogf/ehp)
Across all pages, automate finding common markup patterns within a set
threshold, build a documented component library for most common patterns.

