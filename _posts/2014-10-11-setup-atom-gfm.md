---
layout: post
title: "Setup Atom for using GFM"
categories: articles
modified: 2014-08-27T11:57:41-04:00
tags: [sample]
---

# Install Atom for Windows

Download [Atom Alpha](https://atom.io/) and do the typical Windows install click, click, click...

## Install language-gfm Package

Open the **Settings** menu:

File > Settings

or

Use the keyboard shortcut `Ctrl`+`Comma`

or

Use the keyboard shortcut `Ctrl`+`Shift`+`P`.

Type `settings` in the search box and press `Enter` to display the menu.

Click on **Packages** from the left menu, type `language` in the search box and then select the language-gfm package and click `Install`.

Scroll down the list of installed packages on the left of the settings screen and you will now find **Language Gfm** in the list.

Click on the package name to see the options available.

## Markdown Examples

The following examples demonstrate various features of GFM:

 - [something] todo

| Trigger | Name        | Example   | Result |
|:--------|:-----------:|:---------:|-------:|
| `b`       | bold text   | \*\*$1\*\*$0 | **$1**$0 |
| `i`       | italic text | \*$1\*$0 | *$1*$0   |
| `l`       | link        | \[$1\]\($2\)$0 | [$1]($2)$0 |
| `t`       | todo        | - [ ] $1 | - [todo] $1 |
| `code`    | code        | \`\`\`\$1\\n$2\\n\`\`\`$0 | ```$1\n$2\n```$0 |

### Syntax Highlighting

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```

### Tables

| Left Aligned   | Center Aligned    | Right Aligned |
| :------------- | :---------------: | -----: |
| col 3 is      | some wordy text | $1600 |
| col 2 is      | centered        |   $12 |
| zebra stripes | are neat        |    $1 |

| ${1:Header One } | ${2:Header Two |
|:---------------|:---------------|
| ${3:Item One } | ${4:Item Two } | $0

| Name | Description          |
| ------------- | ----------- |
| Help      | ~~Display the~~ help window.|
| Close     | _Closes_ a window     |

### Task Lists

> The overriding design goal for [Markdown’s formatting syntax](http://daringfireball.net/projects/markdown/) is to make it as readable as possible. The idea is that a Markdown-formatted document should be publishable as-is, as plain text, without looking like it’s been marked up with tags or formatting instructions.

Support for [Task Lists](https://github.com/blog/1375%0A-task-lists-in-gfm-issues-pulls-comments) is available:

- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> are supported
- [x] list syntax is required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item


### HTML

Use a subset of HTML within READMEs, issues, and pull requests.

A full list of supported tags and attributes can be found in the [README for github/markup](https://github.com/github/markup/tree/master#html-sanitization).
