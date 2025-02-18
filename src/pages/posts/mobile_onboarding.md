---
layout: ../../layouts/post.astro
title: 'Get Started With Aggie Events Mobile Dev'
pubDate: 2025-2-10
description: 'Set up and common tools for development on the Aggie Events mobile application.'
author: 'Jadon Lee'
excerpt: 'Set up and common tools for development on the Aggie Events mobile application.'
image:
  src:
  alt:
tags: ['frontend','mobile','Expo','React Native']
---
## Welcome to Mobile Development!

We will be using Expo with React Native for our mobile development.
You can read more about this here: [https://docs.expo.dev/]
Or watch this video for a brief summary: [https://www.youtube.com/watch?v=vFW_TxKLyrE]
Essentially, though, Expo is built on top of reactive native. React native is a cross platform version of React. Expo helps to deploy to Android and iOS easily.

## Prerequisites

Before you can work on the app you will have to have cloned the project to your computer. If you are not familiar with git, I would recommend looking through some git tutorials.

I recommend this one personally for all things branching and commits, but it can overcomplicate remote repositories. [https://learngitbranching.js.org/?locale=en_US](https://learngitbranching.js.org/?locale=en_US)

Make sure you have node.js installed. Once you have node installed, run npm i inside of the terminal in the location of your mobile project.

## Starting Your Preview Server

Run

```bash
npx expo start
```

Notice that it says **development build**. This means expo is attempting to use development build mode. For most frontend changes, you will be able to use expo go. To switch to expo go mode, press s inside of your terminal.

If you scroll up a bit in your terminal you should see a QR. Download the expo go app then scan the QR code. The app will automatically display the live preview if your phone is on the same network as your laptop. You can also press w to start a web preview if you prefer to preview in a web browser, just make sure to change the browser view mode to mobile (inspect element then click on the icon with a phone and laptop).


## Backend

Since we are now using a local backend in conjunction with the frontend mobile for development, you will have to run it locally in order to develop. Follow this guide: https://blog.aggieevents.tech/posts/onboarding in order to do this.

After you get the backend working (I also recommend you make sure it works with the web version of the project first, then test mobile), change the api-url.ts in the config directory in the mobile project to your LAN ip (you can find this where it says what ip the expo go server is coming from). This will allow your mobile device or virtual device to access your locally hosted backend.

## Coming Soon: Development Builds

Currently, the only feature not supported on our expo go preview is authentication. This will be necessary for posting events to the local database.
