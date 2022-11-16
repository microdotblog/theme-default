# The Cards theme for Micro.blog
Cards is a simple theme for Micro.blog.

## Installation
- Set your current them to Blank and Hugo Version to 0.91 in the design section of your blog admin.
- Uninstall any theme that you already have installed.
- Install the Card theme.

## Change Log
Version 1.0.0: Not yet released

## License
Cards is licensed under the MIT license.

## Support
If you have any issues, you can email me at cardtheme@gregorich.me.
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/M4M0DLOZR)

## Add a reply option to your posts
If you would like to add a link to your post where visitors can reply on Micro.blog, I recommend using the "[Conversation on Micro.blog](https://github.com/svendahlstrand/plugin-conversation-on-mb)" plugin by [@sod](https://micro.blog/sod).

-   Install the Plugin
    -   Open Plugins.
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