# Gordian Website built on the ZOLA.386 port


ZOLA.386 is a port of the BOOTSTRA.386 theme and was based on:

- [BOOTSTRA.386](https://kristopolous.github.io/BOOTSTRA.386/): main idea, design.
- [HUGO.386](https://themes.gohugo.io/hugo.386/): item placement.
- [Dinkleberg](https://github.com/rust-br/dinkleberg): internal structure and SEO.
- [after-dark](https://github.com/getzola/after-dark): navbar and minor components.

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

Remember that all descriptions (`config.description` and `page.description`) are shown on the index page, one at the header and the others through the body.

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

