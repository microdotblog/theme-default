# The Cards theme for Micro.blog
Cards is a simple and lightweight theme for Micro.blog.

## Installation
- Set your current theme to Blank and Hugo Version to 0.91 in the design section of your blog admin.
- Uninstall any theme that you already have installed.
- Install the Card theme.

## Support
If you have any issues, you can email me from this [form](https://ericgregorich.com/email/).

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/M4M0DLOZR)

## Making Customizations to the theme
The easiest (and safest) way to customize this theme is to create a new blank theme while the Cards theme is installed. Then, you can customize the templates in your blank theme without changing the Cards theme. Be sure the select your blank theme (whatever you named it) on your Micro.blog Design page.

When updates are pushed out to the Cards theme, the theme files will be updated automatically. Any custom theme files you have in your custom theme will be untouched.

## Add a reply option to your posts
If you would like to add a link to your post where visitors can reply on Micro.blog, I recommend using the "[Conversation on Micro.blog](https://github.com/svendahlstrand/plugin-conversation-on-mb)" plugin by [@sod](https://micro.blog/sod).

-   Install the Plugin
    -   In your Micro.blog settings, open Plugins.
    -   Search for "Conversation."
    -   Install the "Conversation on Micro.blog" plugin by @sod.
    -   Open your Plugins page again and click on the Settings button next to the plugin.
    -   Configure the plugin as you would like.
-   Add the plugin to your page.
    -   Click on Design.
    -   Click on the Edit Custom Themes button.
    -   Select your theme.
    -   Select the layouts/post/single.html file.
    -   Insert this immediately after the {{ .Content }} text.
        -   `<div class="response-options">{{ partial "conversation-link.html" . }}</div>`
    -   Click Update Template to save your changes.

## Add a reply by email option to your posts
If you would like to add a link to your post, visitors can reply by email, I recommend using the "[Reply by email](https://github.com/svendahlstrand/plugin-reply-by-email)" plugin by [@sod](https://micro.blog/sod).

- Install the Plugin
	- Open Plugins.
	- Search for "Reply."
	- Install the "Reply by email" plugin by @sod.
	- Open your Plugins page again and click on the Settings button next to the plugin.
	- Configure the plugin as you would like.
- Add the plugin to your page.
	- Click on Design.
	- Click on the Edit Custom Themes button.
	- Select your theme.
	- Select the layouts/post/single.html file.
	- Insert this immediately after the {{ .Content }} text.
	- `<div class="response-options">{{ partial "reply-by-email.html" . }}</div>`
	- Click Update Template to save your changes.

* If your also using the Conversation plugin, you can put them both together like this:
```html
<div class="response-options">
	{{ partial "conversation-link.html" . }}
	{{ partial "reply-by-email.html" . }}
</div>
```