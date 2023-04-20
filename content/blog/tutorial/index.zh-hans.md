---
title: "指南"
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

本教程提供简单的示例和代码段，以展示如何创建富文本，更多用法请查阅[文档](https://hbstack.dev/zh-hans/)。

<!--more-->

## 安装

**请注意本主题需要安装 Go 和最新的扩展版 Hugo。**

详情请阅读[安装](https://hbstack.dev/zh-hans/docs/getting-started/installation)一文。

## 新增内容

```sh
hugo new blog/new-post/index.md
```

新创建的内容处于草稿状态，发布时需要移除 `draft`参数或者将其设为 `false`。

{{< bootstrap/alert >}}
{{% markdownify %}}
请指定  `--buildDrafts` (`-D`) 标识以预览草稿，如 `hugo server --gc -D --disableFastRender`。
> **npm run dev**  默认会构建草稿内容。
{{% /markdownify %}}
{{< /bootstrap/alert >}}

## 代码块

````markdown
```[lang]
CODE
```
````

{{% bootstrap/collapse "[lang]" %}}
请将 `[lang]` 替换为对应的语言标识，如 `js`、`php`、`go`、`html` 等。
{{% /bootstrap/collapse %}}

```js
console.log('Hello world!')
```

### 代码高亮样式

HB 提供了数十个代码高亮样式，详情请参阅[代码高亮样式模块](https://hbstack.dev/zh-hans/docs/modules/syntax-highlighting/)。

导入对应的样式模块，并重启 Hugo 服务器以完整地载入模块的资源。

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

## 短代码

详情请参阅[短代码](https://hbstack.dev/zh-hans/docs/content/shortcodes/)。

## 部署

领请参阅[部署](https://hbstack.dev/zh-hans/docs/deployment/)以部署你的站点。
