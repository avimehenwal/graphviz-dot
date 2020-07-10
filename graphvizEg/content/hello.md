---
title: My first Blog Post
description: Learning how to use @nuxt/content to create a blog
img: first-blog-post.jpg
alt: my first blog post
dot1: digraph { graph [label="Click on a node or an edge to delete it" labelloc="t", fontsize="20.0" tooltip=" "] node [style="filled"] Node1 [id="NodeId1" label="N1" fillcolor="#d62728"] Node2 [id="NodeId2" label="N2" fillcolor="#1f77b4"] Node3 [id="NodeId3" label="N3" fillcolor="#2ca02c"] Node4 [id="NodeId4" label="N4" fillcolor="#ff7f0e"] Node1 -> Node2 [id="EdgeId12" label="E12"] Node1 -> Node3 [id="EdgeId131" label="E13"] Node2 -> Node3 [id="EdgeId23" label="E23"] Node3 -> Node4 [id="EdgeId34" label="E34"] }
dot2: digraph D { label = "Sample graph" node [style=filled colorscheme=accent8] A [shape=diamond, fillcolor=1] B [shape=box, fillcolor=2] C [shape=circle, fillcolor=3] D [fillcolor=4] A -> B [style=dashed, color=grey] A -> C [color="black:invis:black"] A -> D [penwidth=5, arrowhead=none] }
---

<dot id="sample1" :code="dot2"></dot>

<dot id="sample2" :code="dot1"></dot>

### dot code block

```dot
digraph graphname {
  a -> b;
  b -> c;
  a -> c;
}
```

### Latex

$$c = m + 2$$

### Containers

::: tip
content
:::

::: tip title
content

muliti line
:::

### Emojis

:dog: :+1:

### Abbreviations

This plugin works on MDAST.

More stuff about MDAST.

*[MDAST]: Markdown Abstract Syntax Tree

Empower your NuxtJS application with `@nuxtjs/content` module: write in a `content/` directory and fetch your Markdown, JSON, YAML and CSV files through a MongoDB like API, acting as a **Git-based Headless CMS**.

## Writing content

Learn how to write your `content/`, supporting Markdown, YAML, CSV and JSON: https://content.nuxtjs.org/writing.

## Fetching content

Learn how to fetch your content with `$content`: https://content.nuxtjs.org/fetching.

## Displaying content


Learn how to display your Markdown content with the `<nuxt-content>` component directly in your template: https://content.nuxtjs.org/displaying.

```mermaid
graph LR
    Start --> Stop
```

```dot
digraph graphname {
  a -> b;
  b -> c;
  a -> c;
}
```

* https://github.com/sschoger/heroicons-ui/tree/master/svg

