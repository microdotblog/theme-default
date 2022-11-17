# The Cards theme for Micro.blog
Cards is a simple and lightweight theme for Micro.blog.

## Installation
- Open the Design page in your Micro.blog settings.
- Set your current theme to Blank and Hugo Version to 0.91 in the design section of your blog admin.
- Uninstall any theme that you already have installed.
- Install the Cards theme.

## Support
If you have any issues, you can email me from this [form](https://ericgregorich.com/email/).

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/M4M0DLOZR)

## How to add your own customizations
The easiest (and safest) way to customize this theme is to create a new blank theme while the Cards theme is installed. You can customize the template files in your blank theme without changing the Cards theme.

When updates are pushed out to the Cards theme, the theme files will be updated automatically. Any custom theme files you have in your custom theme will be untouched.

## How to add a reply in Micro.blog option to your posts
If you want to add a link to your post where visitors can reply from Micro.blog, I recommend using the "[Conversation on Micro.blog](https://github.com/svendahlstrand/plugin-conversation-on-mb)" plugin by [@sod](https://micro.blog/sod).

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
    -   Insert this code snippet to your page. After the {{ .Content }} text works well.

```html 
<div class="response-options">{{ partial "conversation-link.html" . }}</div>
```
- Click Update Template to save your changes.

## How to add a reply by email option to your posts
If you want to add a link to your post where visitors can reply to the post using email, I recommend using the "[Reply by email](https://github.com/svendahlstrand/plugin-reply-by-email)" plugin by [@sod](https://micro.blog/sod).

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
	- Insert this code snippet to your page. After the {{ .Content }} text works well.

```html
<div class="response-options">{{ partial "reply-by-email.html" . }}</div>
```

- Click Update Template to save your changes.

> If your also using both plugins (Conversation and Reply by email), you can put them both together by adding this code block. Whether your using one or both plugins, add you partial text inside the response-options Div tag to receive some automatic styling that matches this theme.

```html
<div class="response-options">
	{{ partial "conversation-link.html" . }}
	{{ partial "reply-by-email.html" . }}
</div>
```