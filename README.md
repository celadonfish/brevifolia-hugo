# Brevifolia

<!-- [![Build Status](https://travis-ci.com/EmielH/tale-hugo.svg?branch=master)](https://travis-ci.com/EmielH/tale-hugo) -->

This is a Hugo theme based on the theme [Tale](https://github.com/EmielH/tale-hugo) (which was ported to Hugo from [Tale theme for Jekyll](https://github.com/chesterhow/tale)) and the changes to the Tale theme from the [Brevifolia starter template](https://github.com/kendallstrautman/brevifolia-hugo-forestry).
I did not design this theme, nor the theme it is based on; I only created its own repository for it, so it can be properly added as a submodule in Hugo environments.

## Installation

### 1. Install the theme

If your site is also under version control using git, the easiest way to install this theme is to add it as a submodule. If you have not created a git repo for your project yet, you need to run `git init` beforehand. Inside the folder of your Hugo site, run the following command.

```
git submodule add https://github.com/celadonfish/brevifolia-hugo.git themes/brevifolia
```

Alternatively, you can clone the theme into your project.

```
git clone https://github.com/celadonfish/brevifolia-hugo.git themes/brevifolia
```

### 2. Configure Hugo

Add the following line to `config.toml` to tell Hugo to use the theme.

```
theme = "brevifolia"
```

Alternatively, you can tell Hugo to use the theme with the `server` command.

```
hugo server -t brevifolia
```

### Additional information

For more information, read the official [setup guide](https://gohugo.io/overview/installing/) of Hugo.

### Update the theme

If you have installed the theme as a git submodule, you can update the theme by issuing the following command inside your project folder.

```
git submodule update --remote --rebase
```

If you have cloned the theme, you can run `git pull` inside the theme folder.

## Configuration

<!--
### Menu

The top menu uses [Hugo Menus](https://gohugo.io/content-management/menus/), with the name of the menu being `main`. To turn on the menu, follow the steps there - you can either add something like this to the front-matter of your pages:

```
---
menu: "main"
---
```

... or you can add a menu section to your `config` file:

```
sectionPagesMenu = "main"
```

Or if you want more control, add a specific entry for each item in your menu:

```
[menu]
  [[menu.main]]
    identifier = "about"
    name = "About"
    title = "About"
    url = "/about/"
    weight = 0
  [[menu.main]]
    identifier = "posts"
    name = "Posts"
    title = "Posts"
    url = "/posts/"
    weight = 0
```

For menu internationalization/translation, see [Multilingual Mode: Menus](https://gohugo.io/content-management/multilingual/#menus).
-->

### Internationalisation (i18n)

Brevifolia supports using other languages than English. Language files for the texts Brevifolia uses are provided in the `i18n` directory. The default language is English. To switch languages, add the key `defaultContentLanguage` to your `config.toml` file. For example:

```
defaultContentLanguage = "nl"
```

To translate texts your site uses, add an `i18n` folder to your site.

Feel free to submit pull requests for other translations of Brevifolia's texts.

[Hugo documentation for multilingual sites](//gohugo.io/content-management/multilingual/)

### Disqus
Brevifolia supports Disqus integration, a comment system that empowers dynamic features to static websites. To install it, just add the key `disqusShortname` in your `config.toml`
``` toml
disqusShortname = "disqus-example"
``` 
Add the parameter `comments` in the front-matter of the pages where you want to allow comments 
``` 
---
comments: true
---
```

### Google Analytics

Brevifolia supports Google Analytics integration using Hugo's provided `google_analytics_async` template.

To enable it, add the `googleAnalytics` tag to your `config.toml`. It will be added on all pages.

```toml
googleAnalytics = "UA-133700000-0"
```

### Custom summaries

Brevifolia allows for writing the summary of your posts manually by setting the `summary` variable in the page frontmatter. If this variable is not set, the summary that Hugo automatically generates will be used.

### Taxonomies

Brevifolia has basic support for taxonomies. Taxonomy and terms pages will be generated when you have defined taxonomies, but you need to include links to these pages yourself. For example, you can add a link to a taxonomy page in `header-menu.html`.

### Placeholder partials

The theme contains placeholder partials to make the theme more flexible and easier to adapt to your site without having to change the theme itself. These are:

- `single/header.html`
- `single/footer.html`

These are included in the template for a single post, at the top of the post (below the title) and at the bottom of the post, respectively. These can be used, for example, to include additional information about the post author or for related posts. Create a file `/layouts/partials/single/header.html` or `footer.html` on your own site to have it included.

- `index/introduction.html`

This partial is included at the top of the list of posts on the index page, allowing you to add an introduction to your site.

### Copyright message

The copyright message in the footer uses the name of the author of the site, as defined in `config.toml`. For example:

```
[Author]
    name = "Emiel"
```

### Additional CSS files

The theme can load additional CSS files for you, e.g. to override some of the styles, or the CSS that goes with a component that you're using. To add additional CSS files, put these files in the `static` folder of your site and add the `css` parameter to `config.toml`, like so:

```
[Params]
css = ["custom.css"]
```

To load multiple CSS files, use the parameter like this:

```
[Params]
css = ["custom.css", "custom2.css"]
```

## Roadmap

Some more planned features for this theme:

- RSS support
- Inline Math/LaTeX rendering
- Webring integration

## Acknowledgments

Thanks

- to [Chester How](//github.com/chesterhow) for creating the original [Tale theme for Jekyll](https://chesterhow.github.io/tale/),
- to [onedrawingperday](//github.com/onedrawingperday), [bep](//github.com/bep) and [digitalcraftsman](//github.com/digitalcraftsman) for their help in getting the theme working correctly with Hugo,
- to [lucperkins](https://github.com/lucperkins) for the [Fresh theme](https://github.com/lucperkins/hugo-fresh) from which I used some useful snippets of code.
- to [EmielH](https://github.com/EmielH) for the port at [tale-hugo](https://github.com/EmielH/tale-hugo).
- to [kendallstrautman](https://github.com/kendallstrautman) for the changes to the theme in [brevifolia-hugo-forestry](https://github.com/kendallstrautman/brevifolia-hugo-forestry).

## License
See [LICENSE](https://github.com/EmielH/tale-hugo/blob/master/LICENSE).
