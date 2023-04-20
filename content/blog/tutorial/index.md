---
title: "Tutorial"
# linkTitle:
date: 2023-03-31T11:47:31+08:00
draft: false
description: 
noindex: false
pinned: true
nav_weight: 1000
# nav_icon:
#   vendor: bootstrap
#   name: toggles
#   color: '#e24d0e'
series:
  - Tutorial
categories:
  - Content
tags:
  - Shortcode
  - Code Block
  - KaTex
  - Mermaid
  - Math
  - Diagram
images:
# menu:
#   main:
#     weight: 100
#     params:
#       icon:
#         vendor: bs
#         name: book
#         color: '#e24d0e'
authors:
  - razonyang
  - hugomods
---

A simple tutorial that offers samples and code snippets show how to create rich content, please refer to the [documentations](https://hbstack.dev/en/) for more usage.

<!--more-->

## Installation

**Please note that this theme requires Go installation the newest extended Hugo version.**

Please check out the [installation](https://hbstack.dev/en/docs/getting-started/installation/) section.

## Create Content

```sh
hugo new blog/new-post/index.md
```

The created content is in draft stage, you'll need to publish the content by removing the `draft` or setting the `draft` as `true` on front matter. Learn on on [content](https://hbstack.dev/en/docs/content/).

## Code Block

````markdown
```[lang]
CODE
```
````

{{% bootstrap/collapse "[lang]" %}}
Replace `[lang]` with corresponding language identifier, such as `js`, `php`, `go`, `html` and so on.
{{% /bootstrap/collapse %}}

```js
console.log('Hello world!')
```

### Code Syntax Highlighting Styles

HB offers dozens of syntax highlighting styles, find more on [syntax highlighting styles modules](https://hbstack.dev/en/docs/modules/syntax-highlighting/).

Import the desired style module and restart the Hugo server (load module's assets fully) to preview.

{{< bootstrap/config-toggle hugo >}}
module:
  imports:
    - path: github.com/hbstack/syntax-highlighting/styles/github-dark
{{< /bootstrap/config-toggle >}}

## KaTex

````markdown
```katex
MATH
```
````

```katex
f(x) = \int_{-\infty}^\infty\hat f(\xi)\,e^{2 \pi i \xi x}\,d\xi
```

Read more on [KaTex Usage](https://hugomods.com/en/docs/content/katex/#usage).

## Mermaid

````markdown
```mermaid
DIAGRAM
```
````

```mermaid
graph TD;
  A-->B;
  A-->C;
  B-->D;
  C-->D;
```

Read more on [Mermaid Usage](https://hugomods.com/en/docs/content/mermaid/#usage).

## Shortcodes

Learn more on [shortcodes](https://hbstack.dev/en/docs/content/shortcodes/).

## Deployment

See [deployment](https://hbstack.dev/en/docs/deployment/) for deploying your site.
