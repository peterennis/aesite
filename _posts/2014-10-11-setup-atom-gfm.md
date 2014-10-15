---
layout: post
title: "Setup Atom for using GFM"
categories: articles
modified: 2014-08-27T11:57:41-04:00
tags: [sample]
---

# Install Atom for Windows

Download [Atom Alpha](https://atom.io/) and do the typical Windows install click, click, click...

## Install [language-gfm](https://github.com/atom/language-gfm) Package

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

### Why Markdown?

> The overriding design goal for [Markdown’s formatting syntax](http://daringfireball.net/projects/markdown/) is to make it as readable as possible. The idea is that a Markdown-formatted document should be publishable as-is, as plain text, without looking like it’s been marked up with tags or formatting instructions.
> > This is a nested Markdown blockquote.

When viewing source data for the table examples below the difference in readability is very clear, even for such short samples.

## Markdown Examples

The following examples demonstrate various features of GFM:

Tada :tada: Fireworks :fireworks: !!!

 - [something] todo

| Trigger | Name        | Example   | Result |
|:--------|:-----------:|:---------:|-------:|
| `b`       | bold text   | \*\*$1\*\*$0 | **$1**$0 |
| `i`       | italic text | \*$1\*$0 | *$1*$0   |
| `l`       | link        | \[$1\]\($2\)$0 | [$1]($2)$0 |
| `t`       | todo        | - [ ] $1 | - [todo] $1 |
| `code`    | code        | \`\`\`\$1\\n$2\\n\`\`\`$0 | ```$1\n$2\n```$0 |

### Tables

| Table |
|-------|
| Foo   |

| Left Aligned   | Center Aligned    | Right Aligned |
| :------------- | :---------------: | -----: |
| col 3 is      | some wordy text | $1600 |
| col 2 is      | centered        |   $12 |
| zebra stripes | are neat        |    $1 |

| ${1:Header One } | ${2:Header Two} |
|:---------------|:---------------|
| ${3:Item One } | ${4:Item Two } | $0

| Name | Description          |
| ------------- | ----------- |
| Help      | ~~Display the~~ help window.|
| Close     | _Closes_ a window     |

This is a regular paragraph [example](https://github.com/coapp/coapp.org/blob/master/src/dynamic/reference/garrett-flavored-markdown.html.md) that illustrates creation of a table using HTML tags:

<table>
    <tr>  <td>Foo</td></tr>
</table>

This is a more complex [example](http://www.w3schools.com/html/html_tables.asp) with HTML tags:

<table style="width:100%">
  <tr>
    <th>First Name</th>
     <th>Last Name</th>
    <th>Score</th>
  <tr>
    <td>Jill</td>
     <td>Smith</td>
    <td>50</td>
   </tr>
  <tr>
    <td>Eve</td>
     <td>Jackson</td>
    <td>94</td>
   </tr>
</table>

### Syntax Highlighting

The list of [Syntax-highlighter Languages](http://coapp.org/reference/garrett-flavored-markdown.html) is extensive.

e.g. ruby

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```

e.g. text

```text
Private Sub CountToTen()
  For i = 1 to 10
    Debug.Print i
  Next i
End Sub
```

<table>
      <thead><tr><th>Language</th><th style="width:250px;">Highlight Code</th><th>Language</th><th>Highlight Code</th></tr></thead>
      <tbody>
        <tr><td>ABAP</td><td>abap</td><td>ActionScript</td><td>as</td></tr>
        <tr><td>ActionScript 3</td><td>as3</td><td>Ada</td><td>ada</td></tr>
        <tr><td>ANTLR</td><td>antlr</td><td>ANTLR With ActionScript Target</td><td>antlr-as</td></tr>
        <tr><td>ANTLR With C# Target</td><td>antlr-csharp</td><td>ANTLR With CPP Target</td><td>antlr-cpp</td></tr>
        <tr><td>ANTLR With Java Target</td><td>antlr-java</td><td>ANTLR With ObjectiveC Target</td><td>antlr-objc</td></tr>
        <tr><td>ANTLR With Perl Target</td><td>antlr-perl</td><td>ANTLR With Python Target</td><td>antlr-python</td></tr>
        <tr><td>ANTLR With Ruby Target</td><td>antlr-ruby</td><td>ApacheConf</td><td>apacheconf</td></tr>
        <tr><td>AppleScript</td><td>applescript</td><td>aspx-cs</td><td>aspx-cs</td></tr>
        <tr><td>aspx-vb</td><td>aspx-vb</td><td>Asymptote</td><td>asy</td></tr>
        <tr><td>Bash</td><td>bash</td><td>Bash Session</td><td>console</td></tr>
        <tr><td>Batchfile</td><td>bat</td><td>BBCode</td><td>bbcode</td></tr>
        <tr><td>Befunge</td><td>befunge</td><td>Boo</td><td>boo</td></tr>
        <tr><td>Brainfuck</td><td>brainfuck</td><td>C</td><td>c</td></tr>
        <tr><td>C#</td><td>csharp</td><td>C++</td><td>cpp</td></tr>
        <tr><td>c-objdump</td><td>c-objdump</td><td>cfstatement</td><td>cfs</td></tr>
        <tr><td>Cheetah</td><td>cheetah</td><td>Clojure</td><td>clojure</td></tr>
        <tr><td>CMake</td><td>cmake</td><td>CoffeeScript</td><td>coffee-script</td></tr>
        <tr><td>Coldufsion HTML</td><td>cfm</td><td>Common Lisp</td><td>common-lisp</td></tr>
        <tr><td>cpp-objdump</td><td>cpp-objdump</td><td>CSS</td><td>css</td></tr>
        <tr><td>CSS+Django/Jinja</td><td>css+django</td><td>CSS+Genshi Text</td><td>css+genshitext</td></tr>
        <tr><td>CSS+Mako</td><td>css+mako</td><td>CSS+Myghty</td><td>css+myghty</td></tr>
        <tr><td>CSS+PHP</td><td>css+php</td><td>CSS+Ruby</td><td>css+erb</td></tr>
        <tr><td>CSS+Smarty</td><td>css+smarty</td><td>Cython</td><td>cython</td></tr>
        <tr><td>D</td><td>d</td><td>d-objdump</td><td>d-objdump</td></tr>
        <tr><td>Darcs Patch</td><td>dpatch</td><td>Debian Control file</td><td>control</td></tr>
        <tr><td>Debian Sourcelist</td><td>sourceslist</td><td>Delphi</td><td>delphi</td></tr>
        <tr><td>Diff</td><td>diff</td><td>Django/Jinja</td><td>django</td></tr>
        <tr><td>Dylan</td><td>dylan</td><td>Embedded Ragel</td><td>ragel-em</td></tr>
        <tr><td>ERB</td><td>erb</td><td>Erlang</td><td>erlang</td></tr>
        <tr><td>Erlang erl session</td><td>erl</td><td>Evoque</td><td>evoque</td></tr>
        <tr><td>Felix</td><td>felix</td><td>Fortran</td><td>fortran</td></tr>
        <tr><td>GAS</td><td>gas</td><td>Genshi</td><td>genshi</td></tr>
        <tr><td>Genshi Text</td><td>genshitext</td><td>Gettext Catalog</td><td>pot</td></tr>
        <tr><td>Gherkin</td><td>Cucumber</td><td>GLSL</td><td>glsl</td></tr>
        <tr><td>Gnuplot</td><td>gnuplot</td><td>Go</td><td>go</td></tr>
        <tr><td>Groff</td><td>groff</td><td>Haml</td><td>haml</td></tr>
        <tr><td>Haskell</td><td>haskell</td><td>haXe</td><td>hx</td></tr>
        <tr><td>HTML</td><td>html</td><td>HTML+Cheetah</td><td>html+cheetah</td></tr>
        <tr><td>HTML+Django/Jinja</td><td>html+django</td><td>HTML+Evoque</td><td>html+evoque</td></tr>
        <tr><td>HTML+Genshi</td><td>html+genshi</td><td>HTML+Mako</td><td>html+mako</td></tr>
        <tr><td>HTML+Myghty</td><td>html+myghty</td><td>HTML+PHP</td><td>html+php</td></tr>
        <tr><td>HTML+Smarty</td><td>html+smarty</td><td>INI</td><td>ini</td></tr>
        <tr><td>Io</td><td>io</td><td>IRC logs</td><td>irc</td></tr>
        <tr><td>Java</td><td>java</td><td>Java Server Page</td><td>jsp</td></tr>
        <tr><td>JavaScript</td><td>js</td><td>JavaScript+Cheetah</td><td>js+cheetah</td></tr>
        <tr><td>JavaScript+Django/Jinja</td><td>js+django</td><td>JavaScript+Genshi Text</td><td>js+genshitext</td></tr>
        <tr><td>JavaScript+Mako</td><td>js+mako</td><td>JavaScript+Myghty</td><td>js+myghty</td></tr>
        <tr><td>JavaScript+PHP</td><td>js+php</td><td>JavaScript+Ruby</td><td>js+erb</td></tr>
        <tr><td>JavaScript+Smarty</td><td>js+smarty</td><td>Lighttpd configuration file</td><td>lighty</td></tr>
        <tr><td>Literate Haskell</td><td>lhs</td><td>LLVM</td><td>llvm</td></tr>
        <tr><td>Logtalk</td><td>logtalk</td><td>Lua</td><td>lua</td></tr>
        <tr><td>Makefile</td><td>make</td><td>Makefile (basemake)</td><td>basemake</td></tr>
        <tr><td>Mako</td><td>mako</td><td>Matlab</td><td>matlab</td></tr>
        <tr><td>MiniD</td><td>minid</td><td>Modelica</td><td>modelica</td></tr>
        <tr><td>Modula-2</td><td>modula2</td><td>MoinMoin/Trac Wiki markup</td><td>trac-wiki</td></tr>
        <tr><td>MOOCode</td><td>moocode</td><td>MuPAD</td><td>mupad</td></tr>
        <tr><td>MXML</td><td>mxml</td><td>Myghty</td><td>myghty</td></tr>
        <tr><td>MySQL</td><td>mysql</td><td>NASM</td><td>nasm</td></tr>
        <tr><td>Newspeak</td><td>newspeak</td><td>Nginx configuration file</td><td>nginx</td></tr>
        <tr><td>NumPy</td><td>numpy</td><td>objdump</td><td>objdump</td></tr>
        <tr><td>Objective-C</td><td>objective-c</td><td>Objective-J</td><td>objective-j</td></tr>
        <tr><td>OCaml</td><td>ocaml</td><td>Ooc</td><td>ooc</td></tr>
        <tr><td>Perl</td><td>perl</td><td>PHP</td><td>php</td></tr>
        <tr><td>POVRay</td><td>pov</td><td>Prolog</td><td>prolog</td></tr>
        <tr><td>Python</td><td>python</td><td>Python 3</td><td>python3</td></tr>
        <tr><td>Python 3.0 Traceback</td><td>py3tb</td><td>Python console session</td><td>pycon</td></tr>
        <tr><td>Python Traceback</td><td>pytb</td><td>Raw token data</td><td>raw</td></tr>
        <tr><td>RConsole</td><td>rconsole</td><td>REBOL</td><td>rebol</td></tr>
        <tr><td>Redcode</td><td>redcode</td><td>reStructuredText</td><td>rst</td></tr>
        <tr><td>RHTML</td><td>rhtml</td><td>Ruby</td><td>rb</td></tr>
        <tr><td>Ruby irb session</td><td>rbcon</td><td>S</td><td>splus</td></tr>
        <tr><td>Sass</td><td>sass</td><td>Scala</td><td>scala</td></tr>
        <tr><td>Scheme</td><td>scheme</td><td>Smalltalk</td><td>smalltalk</td></tr>
        <tr><td>Smarty</td><td>smarty</td><td>SQL</td><td>sql</td></tr>
        <tr><td>sqlite3con</td><td>sqlite3</td><td>SquidConf</td><td>squidconf</td></tr>
        <tr><td>Tcl</td><td>tcl</td><td>Tcsh</td><td>tcsh</td></tr>
        <tr><td>TeX</td><td>tex</td><td>Text only</td><td>text</td></tr>
        <tr><td>Vala</td><td>vala</td><td>VB.net</td><td>vb.net</td></tr>
        <tr><td>VimL</td><td>vim</td><td>XML</td><td>xml</td></tr>
        <tr><td>XML+Cheetah</td><td>xml+cheetah</td><td>XML+Django/Jinja</td><td>xml+django</td></tr>
        <tr><td>XML+Evoque</td><td>xml+evoque</td><td>XML+Mako</td><td>xml+mako</td></tr>
        <tr><td>XML+Myghty</td><td>xml+myghty</td><td>XML+PHP</td><td>xml+php</td></tr>
        <tr><td>XML+Ruby</td><td>xml+erb</td><td>XML+Smarty</td><td>xml+smarty</td></tr>
        <tr><td>XSLT</td><td>xslt</td><td>YAML</td><td>yaml</td></tr>
      </tbody>
    </table>

### Task Lists

GitHub issues and pull requests with task list items defined will summarize the task list on the pull request listing and any cross reference.

Support for [Task Lists](https://github.com/blog/1375%0A-task-lists-in-gfm-issues-pulls-comments) is available:

```
- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> are supported
- [x] list syntax is required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item
```

will result in this output:

- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> are supported
- [x] list syntax is required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item

**Nested Task List**

- [ ] a bigger project
  - [ ] first subtask #1234
  - [ ] follow up subtask #4321
  - [ ] final subtask cc @mention
- [ ] a separate task

*   A list item with a blockquote:

    > This is a blockquote
      inside a list item.

### References

Certain [references](https://help.github.com/articles/writing-on-github/#references) are auto-linked:

* SHA: a5c3785ed8d6a35868bc169f07e40e889087fd2e
* User@SHA: jlord@a5c3785ed8d6a35868bc169f07e40e889087fd2e
* User/Repository@SHA: jlord/sheetsee.js@a5c3785ed8d6a35868bc169f07e40e889087fd2e
* #Num: #26
* GH-Num: GH-26
* User#Num: jlord#26
* User/Repository#Num: jlord/sheetsee.js#26

### HTML

Use a subset of HTML within READMEs, issues, and pull requests.

A full list of supported tags and attributes can be found in the [README for github/markup](https://github.com/github/markup/tree/master#html-sanitization).
