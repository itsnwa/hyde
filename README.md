+++

+++
# Hyde

Hyde is a brazen two-column [hugo](https://gohugo.io) theme based on the [Jekyll](http://jekyllrb.com) theme of the same name.
It pairs a prominent sidebar with uncomplicated content.

![Hyde screenshot](https://f.cloud.github.com/assets/98681/1831228/42af6c6a-7384-11e3-98fb-e0b923ee0468.png)

## Installation

You've successfully installed your Hyde Theme in a Hugo project.

There's a few more settings we need to customize before you can get started.

#### 1. Deployment

Currently your site is only visible to you but there's a few options to quickly make your site available to the world.

The easiest option in our opinion is Netlify. It's quick to setup and relatively easy to maintain.

1. Go to [https://app.netlify.com/start](https://app.netlify.com/start "https://app.netlify.com/start")
2. Connect your Git provider and provide Netlify access to your repository (e.g. username/hyde)
3. Select and Click on your repository
4. Enter your build settings.
   * Build Command: `hugo`
   * Publish Directory: `public`
5. Add advanced build settings as a new variable.
   * Key: `HUGO_VERSION` Value: `0.42`
6. Click on `Deploy Site`
7. Lastly copy your URL (e.g. https://something-something-123456.netlify.com) and add it as your URL in your Site's [configuration](/#/pages/config-toml). 

The more powerful option is deployment to AWS and makes sense if you have experience with S3 and Cloudformation.

## Options

Hyde includes some customizable options, typically applied via classes on the `<body>` element.

### Sidebar menu

Create a list of nav links in the sidebar by assigning "menu=main" in the front matter.

### Sticky sidebar content

By default Hyde ships with a sidebar that affixes it's content to the bottom of the sidebar. You can optionally disabled this by removing the `.sidebar-sticky` class from the sidebar's `.container`. Sidebar content will then normally flow from top to bottom.

```html
<!-- Default sidebar -->
<div class="sidebar">
  <div class="container sidebar-sticky">
    ...
  </div>
</div>

<!-- Modified sidebar -->
<div class="sidebar">
  <div class="container">
    ...
  </div>
</div>
```

### Themes

Hyde ships with eight optional themes based on the [base16 color scheme](https://github.com/chriskempson/base16). Apply a theme to change the color scheme (mostly applies to sidebar and links).

![Hyde in red](https://f.cloud.github.com/assets/98681/1831229/42b0b354-7384-11e3-8462-31b8df193fe5.png)

There are eight themes available at this time.

![Hyde theme classes](https://f.cloud.github.com/assets/98681/1817044/e5b0ec06-6f68-11e3-83d7-acd1942797a1.png)

To use a theme, add the `themeColor` variable under `params`, like so:

**TOML**

```toml
theme = "hyde"

[params]
  themeColor = "theme-base-09"
```

**YAML**

```yaml
theme: "hyde"

params:
  themeColor: "theme-base-09"
```

To create your own theme, look to the Themes section of [included CSS file](https://github.com/poole/hyde/blob/master/public/css/hyde.css). Copy any existing theme (they're only a few lines of CSS), rename it, and change the provided colors.

### Reverse layout

![Hyde with reverse layout](https://f.cloud.github.com/assets/98681/1831230/42b0d3ac-7384-11e3-8d54-2065afd03f9e.png)

To reverse page orientation, add the `layoutReverse` variable under `params`, like so:

**TOML**

```toml
theme = "hyde"

[params]
  layoutReverse = true
```

**YAML**

```yaml
theme: "hyde"

params:
  layoutReverse: true
```

### Disqus

You can optionally enable a comment system powered by Disqus for the posts. Simply add the variable `disqusShortname` to your config file.

**TOML**

```toml
disqusShortname = "spf13"
```

**YAML**

```yaml
disqusShortname : spf13
```

> **Note:** Previous version 1.0 the Disqus shortname had to be defined inside the `[params]` block.

## Google Analytics

Google Analytics can be enabled by assigning your tracking code to the `googleAnalytics` variable in the config file:

**TOML**

```toml
googleAnalytics = "Your tracking code"
```

**YAML**

```yaml
googleAnalytics: Your tracking code
```

## Author

**Mark Otto**

* [https://github.com/mdo](https://github.com/mdo)
* [https://twitter.com/mdo](https://twitter.com/mdo)

## Ported By

**Steve Francia**

* [https://github.com/spf13](https://github.com/spf13)
* [https://twitter.com/spf13](https://twitter.com/spf13)

## License

Open sourced under the [MIT license](LICENSE.md).

<3