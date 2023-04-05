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

A simple tutorial that offers samples and code snippets show how to create rich content.

<!--more-->

## 安装

Please check out the [installation](https://hb.hugomods.com/en/docs/getting-started/installation) section.

### 安装依赖

```sh
npm ci
```

或者全局安装。

```sh
sudo npm i -g postcss-cli @fullhuman/postcss-purgecss autoprefixer rtlcss
```

后者最适合多个 HB 站点，因为它需要执行一次。两个都成立，选一个你喜欢的。

### 启动 Hugo 服务器

```sh
npm run dev
```

现在可以通过 http://localhost:1313 访问站点。

{{< bootstrap/alert >}}
{{% markdownify %}}
该模板预定义了一个 **npm run prod** 脚本，用于预览生产环境的站点，其可以通过 http://localhost:1314 进行访问。
{{% /markdownify %}}
{{< /bootstrap/alert >}}

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

HB 提供了数十个代码高亮样式，详情请参阅[代码高亮样式模块](https://hb.hugomods.com/en/docs/modules/syntax-highlighting/)。

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

除了 Hugo 内置的短代码外，HB 集成了 [Bootstrap](https://hugomods.com/en/docs/bootstrap/) 模块，其提供了一些使用的短代码。

- [Alert Shortcode](https://hugomods.com/en/docs/bootstrap/alert/).
- [Clearfix Shortcode](https://hugomods.com/en/docs/bootstrap/clearfix/).
- [Collapse Shortcode](https://hugomods.com/en/docs/bootstrap/collapse/).
- [Config Toggle Shortcode](https://hugomods.com/en/docs/bootstrap/config-toggle/).
- [Toggle Shortcode](https://hugomods.com/en/docs/bootstrap/toggle/).
