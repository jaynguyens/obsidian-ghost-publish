# Obsidian Ghost Publish

Plugin for publish to [Ghost](https://ghost.org/) site for [Obsidian](https://obsidian.md/) with a single click.

## How to use

- Create a custom integration follow this [link](https://ghost.org/integrations/custom-integrations/). You would need an **Admin API Key** and **API URL**.
- Once you install the plugin, enable the plugin and add the API KEy and API URL to the setting.
- That's it! you now are able to publish the current document by click on the ghost icon on the sidebar or use the command pallete (CMD+P).

## Frontmatter format

Obsidian Ghost Publish use frontmatter to specify on how you want to publish your post.

At the moment, the format is limited to:

```md
title: string (default: file name)
tags: (default: [])
- tag1
- tag2
featured: boolean (default: false)
published: boolean (default: false)
excerpt: string (default: undefined)
feature_image: string (default: undefined)
```

Note:

- `published` will allows you to specify if you want to publish a post now or draft a post.

### How to run on dev

- Clone this repo.
- `npm i` or `yarn` to install dependencies
- `npm run dev` to start compilation in watch mode.

### Manually installing the plugin

- Run `npm run build`
- Copy over `main.js` and `manifest.json` to your vault `VaultFolder/.obsidian/plugins/your-plugin-id/`.

### Publishing your first article to ghost.

After installing the plugin as described above, you want to publish your first article.
To do that, the plugin uses front matter as a source of metadata. 

At the top of your artical start with: 
```
---
title: string
tags: 
- tag1
- tag2
featured: boolean
published: boolean
excerpt: string
--- 
``` 

the absolute minimum you should use to send your article to gost is:

`title: <title of your article>`

### Issues & Requests

- For feature requests, please take use of Discussions.
- For any issues with current versions, please use Issues.
