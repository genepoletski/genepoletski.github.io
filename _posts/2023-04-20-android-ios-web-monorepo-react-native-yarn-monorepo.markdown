---
layout: post
group_title: Android, iOS and Web App Monorepo with React Native
title: Yarn monorepo
date: 2023-04-20 21:00:00 +1200
category: Software Developement
permalink: /:categories/:slug
---

## Prerequsites
- <a href="https://nodejs.org/en" target="_blank">NodeJS, v18+</a>
- <a href="https://yarnpkg.com" target="_blank">Yarn, v1.22+</a>

## Set up yarn monorepo root
Let's start with creating the project monorepo. I am going to use github and yarn. Starting from now I will be using this repo for the project: 
<a href="https://github.com/genepoletski/android-ios-web-monorepo-react-native" target="_blank">android-ios-web-monorepo-react-native</a>.

Create the project root folder and switch to it
{% highlight console %}
$ mkdir android-ios-web-monorepo-react-native
$ cd android-ios-web-monorepo-react-native
{% endhighlight %}

The next command will create a *package.json* file. Answering to prompts choose all the default values, except for **private**, which we should have set to **true**. Because yarn workspaces are not meant to be published <a href="https://classic.yarnpkg.com/lang/en/docs/workspaces/#toc-how-to-use-it" target="_blank">by design</a>.

{% highlight console %}
$ yarn init
{% endhighlight %}

After we finished our *package.json* will look like this*
{% highlight json %}
{
  "name": "android-ios-web-monorepo-react-native",
  "version": "1.0.0",
  "main": "index.js",
  "license": "MIT",
  "private": true
}
{% endhighlight %}

Project code on <a href="https://github.com/genepoletski/android-ios-web-monorepo-react-native/commit/395547eca83962723259bccd1e011b9dc3d86e4e" target="_blank">github</a>.

That was a good start!

<br />
{% include divider.html %}
<sub>(*) If you initialized git in a new project folder, then you may discover more properties in _package.json_ (ex: **author** or **repository**). I excluded them on purpose to keep the sample lean.</sub>