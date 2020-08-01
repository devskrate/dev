_Jekflix_ comes with features to help you create/edit/share content and provide a nice experience for your visitors.

- [Live Search](https://github.com/thiagorossener/jekflix-template/wiki/Features#live-search)
- [Estimated Reading Time](https://github.com/thiagorossener/jekflix-template/wiki/Features#estimated-reading-time)
- [Reading Progress Bar](https://github.com/thiagorossener/jekflix-template/wiki/Features#reading-progress-bar) *(optional)*
- ["New Post" tag](https://github.com/thiagorossener/jekflix-template/wiki/Features#new-post-tag)
- [Load images on demand](https://github.com/thiagorossener/jekflix-template/wiki/Features#load-images-on-demand)
- [Push Menu](https://github.com/thiagorossener/jekflix-template/wiki/Features#push-menu)
- [SVG icons](https://github.com/thiagorossener/jekflix-template/wiki/Features#svg-icons)
- [Shell script to create posts](https://github.com/thiagorossener/jekflix-template/wiki/Features#shell-script-to-create-posts)
- [Tags page](https://github.com/thiagorossener/jekflix-template/wiki/Features#tags-page)
- [About page](https://github.com/thiagorossener/jekflix-template/wiki/Features#about-page)
- [Contact page](https://github.com/thiagorossener/jekflix-template/wiki/Features#contact-page)
- [404 error page](https://github.com/thiagorossener/jekflix-template/wiki/Features#404-error-page)
- [Feed RSS](https://github.com/thiagorossener/jekflix-template/wiki/Features#feed-rss)
- [Disqus](https://github.com/thiagorossener/jekflix-template/wiki/Features#disqus) *(optional)*
- [Featured post](https://github.com/thiagorossener/jekflix-template/wiki/Features#featured-post) *(optional)*
- [Home page pagination](https://github.com/thiagorossener/jekflix-template/wiki/Features#home-page-pagination) *(optional)*
- [Posts sidebar](https://github.com/thiagorossener/jekflix-template/wiki/Features#posts-sidebar) *(optional)*
- [Paginated posts](https://github.com/thiagorossener/jekflix-template/wiki/Features#paginated-posts) *(optional)*
- ["Before you go" modal](https://github.com/thiagorossener/jekflix-template/wiki/Features#before-you-go-modal) *(optional)*
- [Post recommendation](https://github.com/thiagorossener/jekflix-template/wiki/Features#post-recommendation)
- [Netlify CMS ready](https://github.com/thiagorossener/jekflix-template/wiki/Features#netlify-cms-ready)
- [Translations](https://github.com/thiagorossener/jekflix-template/wiki/setup#translations)
- [Math Expressions](https://github.com/thiagorossener/jekflix-template/wiki/Features#math-expressions) *(optional)*

## Live Search

Located in the top right corner of the template, the search component looks for post titles, categories and tags. It's a simple search for static websites.

![Search Box Screenshot](https://res.cloudinary.com/dm7h7e8xj/image/upload/v1566426001/search-screenshot_sc5edu.jpg)

## Estimated Reading Time

Every post shows an estimated reading time above its title, the minutes are calculated based on an average reader speed.

![Estimated Reading Time Screenshot](https://res.cloudinary.com/dm7h7e8xj/image/upload/v1566426097/minutes-to-read-screenshot_akvu69.jpg)

## Reading Progress Bar

*(Optional)*

It also shows a reading progress bar based on the reading time and the scroll position in the page.

![Reading Progress Bar Screenshot](https://res.cloudinary.com/dm7h7e8xj/image/upload/v1566425470/progress-bar-screenshot_gem7xb.jpg)

You can show/hide the time bar, see the [docs](https://github.com/thiagorossener/jekflix-template/wiki/settings#show_time_bar).

## "New Post" tag

For posts released up to 7 days before the current date, a tag where reads "New Post" is attached to them in the home page.

![New Post Tag Screenshot](https://res.cloudinary.com/dm7h7e8xj/image/upload/v1566425920/new-post-tag-screenshot_nyuycr.jpg)

## Load images on demand

To improve performance in the home page, only the posts above the fold are loaded initially. The next posts are loaded when scrolling down as needed.

![Loading Screenshot](https://res.cloudinary.com/dm7h7e8xj/image/upload/v1566426573/loading-screenshot_akchmx.jpg)

## Push Menu

The template menu is hidden by default and pushes the content to the right when open.

![Menu Screenshot](https://res.cloudinary.com/dm7h7e8xj/image/upload/v1566426941/menu-screenshot_qsoz1z.jpg)

## SVG icons

All icons used in the template are SVGs, providing a nice look for every resolution.

![Template Icons](https://res.cloudinary.com/dm7h7e8xj/image/upload/v1566427250/icons-screenshot_uhk80e.jpg)

## Shell script to create posts

A script named [initpost.sh](https://github.com/thiagorossener/jekflix-template/blob/master/initpost.sh) is provided to make it easier to create posts by command line.

In the project directory, just run:

```
$ ./initpost.sh -c "New post title"
```

## Tags page

All tags are gathered in a single page where visitors can find the blog posts separate by its tags.

![Tags Page Screenshot](https://res.cloudinary.com/dm7h7e8xj/image/upload/v1566430436/tags-page-screenshot_eeyyt8.jpg)

Check it out [here](https://jekflix.rossener.com/tags/).

## About page

An About page is provided by default, you can delete it at any moment.

![About Page Screenshot](https://res.cloudinary.com/dm7h7e8xj/image/upload/v1566430703/about-page-screenshot_rgchze.jpg)

Check it out [here](https://jekflix.rossener.com/about/).

## Contact page

A contact form created with Vue is present in the template, so you don't have to do it from scratch.

![Contact Page Screenshot](https://res.cloudinary.com/dm7h7e8xj/image/upload/v1566476192/contact-page-screenshot_efux2y.jpg)

Check it out [here](https://jekflix.rossener.com/contact/).

## 404 error page

The template also handles 404 errors already.

![404 Page Screenshot](https://res.cloudinary.com/dm7h7e8xj/image/upload/v1566476323/404-page-screenshot_qiieyi.jpg)

Check it out [here](https://jekflix.rossener.com/404/).

## Feed RSS

A feed file is automatically generated on every build.

Check it out a sample [here](https://jekflix.rossener.com/feed.xml).

## Disqus

*(Optional)*

Jekflix Template implements the Disqus plugin, allowing visitors to comment in posts.

See the [docs](https://github.com/thiagorossener/jekflix-template/wiki/settings#disqus_username) to configure it.

## Featured post

*(Optional)*

In this 2.0 version, a hero lockup got added to the home page, like Netflix does with movies.

To turn on/off this feature, see the [docs](https://github.com/thiagorossener/jekflix-template/wiki/settings#show_hero).

![Page with hero screenshot](https://res.cloudinary.com/dm7h7e8xj/image/upload/v1566477681/page-with-hero-screenshot_ixyjzp.jpg)

## Home page pagination

*(Optional)*

There are two different options to show the posts in the home page, the first one is loading new posts when scrolling down and the second one is adding pagination.

To add pagination, see the [docs](https://github.com/thiagorossener/jekflix-template/wiki/settings#paginate).

## Posts sidebar

*(Optional)*

As many people has asked for, Jekflix Template 2.0 adds an optional sidebar to posts.

To show/hide the sidebar, see the [docs](https://github.com/thiagorossener/jekflix-template/wiki/settings#two_columns_layout).

![Post with two columns screenshot](https://res.cloudinary.com/dm7h7e8xj/image/upload/v1566476793/two-columns-screenshot_phumrl.jpg)

## Paginated posts

*(Optional)*

You can also boost your advertising views by paginating posts.

To break your posts into different pages, see the [docs](https://github.com/thiagorossener/jekflix-template/wiki/Post#paginate).

![Paginated Page Screenshot](https://res.cloudinary.com/dm7h7e8xj/image/upload/v1566430021/paginated-page-screenshot_zx4xjn.jpg)

## "Before you go" modal

*(Optional)*

To keep visitors interested in your content, you can show them some posts recommendations before they leave the page or/and they reach the post end.

See the [docs](https://github.com/thiagorossener/jekflix-template/wiki/settings#show_modal_on_exit) for more information.

![Modal screenshot](https://res.cloudinary.com/dm7h7e8xj/image/upload/v1566478245/before-you-go-screenshot_prrplk.jpg)

## Post recommendation

By default, all posts show a post recommendation when visitor reaches the end of the article, like:

![Recommendation Screenshot](https://res.cloudinary.com/dm7h7e8xj/image/upload/v1566478555/recommendation-screenshot_wzhchs.jpg)

This feature is supposed to be similar to the Netflix recommendation when you finish a movie or serie episode.

## Math Expressions

*(Optional)*

*Jekflix Template 3.1.0* now supports math expressions through [MathJax](https://www.mathjax.org/) library, thanks to **[@XieGuochao](https://github.com/XieGuochao)**.

You only need 2 steps:

1. Set `math: true` for a post.
2. Adopt the _MathJax_'s grammar for $\LaTeX$.

For example, `$\sum_{i=1}{10} = 55$` will be rendered as <img src="https://res.cloudinary.com/dm7h7e8xj/image/upload/c_scale,q_78,w_270/v1585835744/Screen_Shot_2020-04-02_at_10.55.24_uafb07.jpg" width="135">.

## Netlify CMS ready

The newest addition to the *Jekflix Template 2.0.0* is the Netlify CMS integration.

With Netlify CMS you will be able to create/edit posts using an editor, access a workflow panel and change every aspect of your blog with some clicks.

To use the Netlify CMS, you need to go through some steps first. See the [docs](https://github.com/thiagorossener/jekflix-template/wiki/Netlify-CMS) for more info.

Here are some screenshots:

![Netlify CMS post list screenshot](https://res.cloudinary.com/dm7h7e8xj/image/upload/v1566479287/netlify-page-1_a0qezm.jpg)

![Netlify CMS post edition screenshot](https://res.cloudinary.com/dm7h7e8xj/image/upload/v1566479287/netlify-page-2_aupygb.jpg)

![Netlify CMS workflow screenshot](https://res.cloudinary.com/dm7h7e8xj/image/upload/v1566479287/netlify-page-3_bj5sks.jpg)

![Netlify CMS site settings screenshot](https://res.cloudinary.com/dm7h7e8xj/image/upload/v1566479287/netlify-page-4_ycfqdp.jpg)

![Netlify CMS theme settings screenshot](https://res.cloudinary.com/dm7h7e8xj/image/upload/v1566479287/netlify-page-5_k6dan9.jpg)