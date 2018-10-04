# Hyde

Hyde is a brazen two-column [hugo](https://gohugo.io) theme based on the [Jekyll](http://jekyllrb.com) theme of the same name. It pairs a prominent sidebar with uncomplicated content.

![Hyde screenshot](https://f.cloud.github.com/assets/98681/1831228/42af6c6a-7384-11e3-98fb-e0b923ee0468.png)

## First Steps

You've successfully installed your Hyde Theme in a Hugo project.

There's a few more settings we need to customize before you can get started.

### 1. Deployment

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
7. Lastly copy your URL (e.g. https://something-something-123456.netlify.com/) and add it as your URL in your `Site Configuration` (the link is in the Sidebar).

The more powerful option is deployment to AWS and makes sense if you have experience with S3 and Cloudformation. You can find detailed documentation and a deployment template [here](https://forestry.io/docs/hosting/s3-cloudfront-stack/).

### 2. Advanced Settings

#### Themes

Hyde ships with eight optional themes based on the [base16 color scheme](https://github.com/chriskempson/base16). Apply a theme to change the color scheme (mostly applies to sidebar and links).

![Hyde in red](https://f.cloud.github.com/assets/98681/1831229/42b0b354-7384-11e3-8462-31b8df193fe5.png)

There are eight themes available at this time.

![Hyde theme classes](https://f.cloud.github.com/assets/98681/1817044/e5b0ec06-6f68-11e3-83d7-acd1942797a1.png)

To use a theme, go to `Site Configuration` -> `Additional Settings` -> `Theme` -> Add one of the theme names above.

To create your own theme, look to the Themes section of [included CSS file](https://github.com/poole/hyde/blob/master/public/css/hyde.css). Copy any existing theme (they're only a few lines of CSS), rename it, and change the provided colors.

#### Reverse layout

![Hyde with reverse layout](https://f.cloud.github.com/assets/98681/1831230/42b0d3ac-7384-11e3-8d54-2065afd03f9e.png)

To reverse page orientation activate `Reverse Layout` in `Site Configuration` -> `Additional Settings`.

#### Commentary with Disqus

You can optionally enable a comment system powered by Disqus for your posts. Simply add your Disqus Shortname in `Site Configuration` -> `Additional Settings` -> `Disqus Shortname`.

#### Google Analytics

Google Analytics can be enabled by assigning your tracking code to `Site Configuration` -> `Additional Settings` -> `Google Analytics Tracking Code`.

If you don't have a Google Analytics Account you can sign up for an account [here](https://marketingplatform.google.com/about/analytics/).

### 3. Editing in Forestry

Your site is completely editable in Forestry. The Hyde theme is a simple responsive blog completely based on posts and a sidebar menu.

#### Creating and Editing A New Page/Post

Pages and Posts are separated into two different categories as Pages are supposed to be listed in the sidebar menu and Posts are only listed in the main window on your site. 

***

### Author

**Mark Otto**

* [https://github.com/mdo](https://github.com/mdo "https://github.com/mdo")
* [https://twitter.com/mdo](https://twitter.com/mdo "https://twitter.com/mdo")

### Ported By

**Steve Francia**

* [https://github.com/spf13](https://github.com/spf13 "https://github.com/spf13")
* [https://twitter.com/spf13](https://twitter.com/spf13 "https://twitter.com/spf13")

### License

Open sourced under the [MIT license](LICENSE.md).

<3
