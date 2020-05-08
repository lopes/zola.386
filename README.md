# ZOLA.386

![ZOLA.386 screenshot](https://github.com/lopes/zola.386/blob/master/screenshot.png?raw=true)

ZOLA.386 is a port of the BOOTSTRA.386 theme and was based on:

- [BOOTSTRA.386](https://kristopolous.github.io/BOOTSTRA.386/): main idea, design.
- [HUGO.386](https://themes.gohugo.io/hugo.386/): item placement.
- [Dinkleberg](https://github.com/rust-br/dinkleberg): internal structure and SEO.
- [after-dark](https://github.com/getzola/after-dark): navbar and minor components.

ZOLA.386 is a theme that refers to the 90s, but with cutting edge features to be fast and responsive.


## Instalation
The easiest way to install ZOLA.386 is to clone this repository and build your site upon it:

```bash
$ git clone https://github.com/lopes/zola.386
```

Of course you can install it just as another theme for your site, but ZOLA.386 must be added as a module:

```bash
$ cd themes
$ git clone https://github.com/lopes/zola.386.git
```


## Configuration
Configuration is mainly done in `config.toml` and here I'll describe the main topics.

### Global
`config.toml` starts with the global variables.  All of these items are important, but it is fundamental to create two taxonomies at least:

```toml
taxonomies = [
  {name="categories", rss=true},
  {name="tags", rss=true},
]
```

### Extras
ZOLA.386 comes with a lot of extra variables which eases the creation and maintenance of the site, so it's important to review all of them after installing the theme.

The `zola386_menu` composes the navbar and is created by setting up a `path`, which will be appended to the `base_url` and the `name` will appear on the navbar.

```toml
zola386_menu = [
  {path="/", name="Home"},
  {path="categories", name="Categories"},
  {path="tags", name="Tags"},
  {path="about", name="About"},
]
```

ZOLA.386 is also prepared to deal with Google Analytics, Disqus, and Twitter --[Open Graph Protocol](https://ogp.me/) is welcome.  Under the `label_` variables, you can set names to better localize your site.  A theme to provide information for its owner and SEO-friendly.

### Other files
The `content\_index.md` file must be properly configured to provide better experience.  Check out this file for more information.


## License
This theme is released under the MIT license.  For more information read the [License](https://github.com/lopes/zola.386/blob/master/LICENSE).
