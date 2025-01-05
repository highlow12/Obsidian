---
title: "hoarder-app/hoarder: A self-hostable bookmark-everything app (links, notes and images) with AI-based automatic tagging and full text search"
source: "https://github.com/hoarder-app/hoarder"
author:
  - "[[GitHub]]"
published:
created: 2025-01-05
description: "A self-hostable bookmark-everything app (links, notes and images) with AI-based automatic tagging and full text search - hoarder-app/hoarder"
tags:
  - "clippings"
---
[![GitHub Actions Workflow Status](https://camo.githubusercontent.com/83f29e9f0c3d64fc76e56ac63a93f447169de7918f0aac661630754a14294026/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f616374696f6e732f776f726b666c6f772f7374617475732f686f61726465722d6170702f686f61726465722f63692e796d6c)](https://github.com/hoarder-app/hoarder/actions/workflows/ci.yml)[![GitHub Release](https://camo.githubusercontent.com/cd30ab4010b24a18d59c92ca72b3ad8525cb05943dc8908b0d858718735e82a9/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f762f72656c656173652f686f61726465722d6170702f686f6172646572) ](https://github.com/hoarder-app/hoarder/releases)[![Discord](https://camo.githubusercontent.com/b05a4815d3520dff25cb2ab98a6a20f6c0592439c94a2c6c6bb84918ff320fad/68747470733a2f2f696d672e736869656c64732e696f2f646973636f72642f313232333638313330383936323732313830323f6c6162656c3d636861742532306f6e253230646973636f7264) ](https://discord.gg/NrgeYywsFh)[![Translation status](https://camo.githubusercontent.com/1e4f97add5d32fcfe8a743d8690cead08b7b8c699e6b1a8b14255ff5f06c5629/68747470733a2f2f686f737465642e7765626c6174652e6f72672f7769646765742f686f61726465722f686f61726465722f7376672d62616467652e737667)](https://hosted.weblate.org/engage/hoarder/)

## [![](https://github.com/hoarder-app/hoarder/raw/main/screenshots/logo.png)](https://github.com/hoarder-app/hoarder/blob/main/screenshots/logo.png)A self-hostable bookmark-everything app with a touch of AI for the data hoarders out there.

[![homepage screenshot](https://github.com/hoarder-app/hoarder/raw/main/screenshots/homepage.png?raw=true)](https://github.com/hoarder-app/hoarder/blob/main/screenshots/homepage.png?raw=true)

## Features

- 🔗 Bookmark links, take simple notes and store images and pdfs.
- ⬇️ Automatic fetching for link titles, descriptions and images.
- 📋 Sort your bookmarks into lists.
- 🔎 Full text search of all the content stored.
- ✨ AI-based (aka chatgpt) automatic tagging. With supports for local models using ollama!
- 🎆 OCR for extracting text from images.
- 🔖 [Chrome plugin](https://chromewebstore.google.com/detail/hoarder/kgcjekpmcjjogibpjebkhaanilehneje) and [Firefox addon](https://addons.mozilla.org/en-US/firefox/addon/hoarder/) for quick bookmarking.
- 📱 An [iOS app](https://apps.apple.com/us/app/hoarder-app/id6479258022), and an [Android app](https://play.google.com/store/apps/details?id=app.hoarder.hoardermobile&pcampaignid=web_share).
- 📰 Auto hoarding from RSS feeds.
- 🔌 REST API.
- 🌐 Mutli-language support.
- 🖍️ Mark and store highlights from your hoarded content.
- 🗄️ Full page archival (using [monolith](https://github.com/Y2Z/monolith)) to protect against link rot. Auto video archiving using [youtube-dl](https://github.com/marado/youtube-dl).
- ☑️ Bulk actions support.
- 🔐 SSO support.
- 🌙 Dark mode support.
- 💾 Self-hosting first.
- \[Planned\] Downloading the content for offline reading in the mobile app.

**⚠️ This app is under heavy development and it's far from stable.**

## Documentation

- [Installation](https://docs.hoarder.app/Installation/docker)
- [Configuration](https://docs.hoarder.app/configuration)
- [Screenshots](https://docs.hoarder.app/screenshots)
- [Security Considerations](https://docs.hoarder.app/security-considerations)
- [Development](https://docs.hoarder.app/Development/setup)

## Demo

You can access the demo at [https://try.hoarder.app](https://try.hoarder.app/). Login with the following creds:

```
email: demo@hoarder.app
password: demodemo
```

The demo is seeded with some content, but it's in read-only mode to prevent abuse.

## Stack

- [NextJS](https://nextjs.org/) for the web app. Using app router.
- [Drizzle](https://orm.drizzle.team/) for the database and its migrations.
- [NextAuth](https://next-auth.js.org/) for authentication.
- [tRPC](https://trpc.io/) for client->server communication.
- [Puppeteer](https://pptr.dev/) for crawling the bookmarks.
- [OpenAI](https://openai.com/) because AI is so hot right now.
- [Meilisearch](https://meilisearch.com/) for the full content search.

## Why did I build it?

I browse reddit, twitter and hackernews a lot from my phone. I frequently find interesting stuff (articles, tools, etc) that I'd like to bookmark and read later when I'm in front of a laptop. Typical read-it-later apps usecase. Initially, I was using [Pocket](https://getpocket.com/) for that. Then I got into self-hosting and I wanted to self-host this usecase. I used [memos](https://github.com/usememos/memos) for those quick notes and I loved it but it was lacking some features that I found important for that usecase such as link previews and automatic tagging (more on that in the next section).

I'm a systems engineer in my day job (and have been for the past 7 years). I didn't want to get too detached from the web development world. I decided to build this app as a way to keep my hand dirty with web development, and at the same time, build something that I care about and use every day.

## Alternatives

- [memos](https://github.com/usememos/memos): I love memos. I have it running on my home server and it's one of my most used self-hosted apps. It doesn't, however, archive or preview the links shared in it. It's just that I dump a lot of links there and I'd have loved if I'd be able to figure which link is that by just looking at my timeline. Also, given the variety of things I dump there, I'd have loved if it does some sort of automatic tagging for what I save there. This is exactly the usecase that I'm trying to tackle with Hoarder.
- [mymind](https://mymind.com/): Mymind is the closest alternative to this project and from where I drew a lot of inspirations. It's a commercial product though.
- [raindrop](https://raindrop.io/): A polished open source bookmark manager that supports links, images and files. It's not self-hostable though.
- Bookmark managers (mostly focused on bookmarking links):
- [Pocket](https://getpocket.com/): Pocket is what hooked me into the whole idea of read-it-later apps. I used it [a lot](https://blog.mbassem.com/2019/01/27/favorite-articles-2018/). However, I recently got into home-labbing and became obsessed with the idea of running my services in my home server. Hoarder is meant to be a self-hosting first app.
- [Linkwarden](https://linkwarden.app/): An open-source self-hostable bookmark manager that I ran for a bit in my homelab. It's focused mostly on links and supports collaborative collections.
- [Omnivore](https://omnivore.app/): Omnivore is pretty cool open source read-it-later app. Unfortunately, it's heavily dependent on google cloud infra which makes self-hosting it quite hard. They published a [blog post](https://docs.omnivore.app/self-hosting/self-hosting.html) on how to run a minimal omnivore but it was lacking a lot of stuff. Self-hosting doesn't really seem to be a high priority for them, and that's something I care about, so I decided to build an alternative.
- [Wallabag](https://wallabag.it/): Wallabag is a well-established open source read-it-later app written in php and I think it's the common recommendation on reddit for such apps. To be honest, I didn't give it a real shot, and the UI just felt a bit dated for my liking. Honestly, it's probably much more stable and feature complete than this app, but where's the fun in that?
- [Shiori](https://github.com/go-shiori/shiori): Shiori is meant to be an open source pocket clone written in Go. It ticks all the marks but doesn't have my super sophisticated AI-based tagging. (JK, I only found about it after I decided to build my own app, so here we are 🤷).

## Translations

Hoarder uses Weblate for managing translations. If you want to help translate Hoarder, you can do so [here](https://hosted.weblate.org/engage/hoarder/).

## Support

If you're enjoying using Hoarder, drop a ⭐️ on the repo!

[![Buy Me A Coffee](https://camo.githubusercontent.com/7b8f7343bfc6e3c65c7901846637b603fd812f1a5f768d8b0572558bde859eb9/68747470733a2f2f63646e2e6275796d6561636f666665652e636f6d2f627574746f6e732f76322f64656661756c742d79656c6c6f772e706e67)](https://www.buymeacoffee.com/mbassem)

## Star History

[![Star History Chart](https://camo.githubusercontent.com/357d9c838d7b1ba4ac8327a858bda8eb15a45b51427462d79a3be7f83f64adb9/68747470733a2f2f6170692e737461722d686973746f72792e636f6d2f7376673f7265706f733d686f61726465722d6170702f686f617264657226747970653d44617465)](https://star-history.com/#hoarder-app/hoarder&Date)