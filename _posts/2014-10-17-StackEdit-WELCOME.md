<!DOCTYPE HTML>
<!DOCTYPE html PUBLIC "" ""><HTML><HEAD>
<META http-equiv="Content-Type" content="text/html; charset=utf-8"></HEAD>
<BODY abp="0">
<PRE abp="1">Welcome to StackEdit!
===================


Hey! I'm your first Markdown document in **StackEdit**[^stackedit]. Don't delete me, I'm very helpful! I can be recovered anyway in the **Utils** tab of the &lt;i class="icon-cog"&gt;&lt;/i&gt; **Settings** dialog.

----------


Documents
-------------

StackEdit stores your documents in your browser, which means all your documents are automatically saved locally and are accessible **offline!**

&gt; **Note:**

&gt; - StackEdit is accessible offline after the application has been loaded for the first time.
&gt; - Your local documents are not shared between different browsers or computers.
&gt; - Clearing your browser's data may **delete all your local documents!** Make sure your documents are synchronized with **Google Drive** or **Dropbox** (check out the [&lt;i class="icon-refresh"&gt;&lt;/i&gt; Synchronization](#synchronization) section).

#### &lt;i class="icon-file"&gt;&lt;/i&gt; Create a document

The document panel is accessible using the &lt;i class="icon-folder-open"&gt;&lt;/i&gt; button in the navigation bar. You can create a new document by clicking &lt;i class="icon-file"&gt;&lt;/i&gt; **New document** in the document panel.

#### &lt;i class="icon-folder-open"&gt;&lt;/i&gt; Switch to another document

All your local documents are listed in the document panel. You can switch from one to another by clicking a document in the list or you can toggle documents using &lt;kbd&gt;Ctrl+[&lt;/kbd&gt; and &lt;kbd&gt;Ctrl+]&lt;/kbd&gt;.

#### &lt;i class="icon-pencil"&gt;&lt;/i&gt; Rename a document

You can rename the current document by clicking the document title in the navigation bar.

#### &lt;i class="icon-trash"&gt;&lt;/i&gt; Delete a document

You can delete the current document by clicking &lt;i class="icon-trash"&gt;&lt;/i&gt; **Delete document** in the document panel.

#### &lt;i class="icon-hdd"&gt;&lt;/i&gt; Export a document

You can save the current document to a file by clicking &lt;i class="icon-hdd"&gt;&lt;/i&gt; **Export to disk** from the &lt;i class="icon-provider-stackedit"&gt;&lt;/i&gt; menu panel.

&gt; **Tip:** Check out the [&lt;i class="icon-upload"&gt;&lt;/i&gt; Publish a document](#publish-a-document) section for a description of the different output formats.


----------


Synchronization
-------------------

StackEdit can be combined with &lt;i class="icon-provider-gdrive"&gt;&lt;/i&gt; **Google Drive** and &lt;i class="icon-provider-dropbox"&gt;&lt;/i&gt; **Dropbox** to have your documents saved in the *Cloud*. The synchronization mechanism takes care of uploading your modifications or downloading the latest version of your documents.

&gt; **Note:**

&gt; - Full access to **Google Drive** or **Dropbox** is required to be able to import any document in StackEdit. Permission restrictions can be configured in the settings.
&gt; - Imported documents are downloaded in your browser and are not transmitted to a server.
&gt; - If you experience problems saving your documents on Google Drive, check and optionally disable browser extensions, such as Disconnect.

#### &lt;i class="icon-refresh"&gt;&lt;/i&gt; Open a document

You can open a document from &lt;i class="icon-provider-gdrive"&gt;&lt;/i&gt; **Google Drive** or the &lt;i class="icon-provider-dropbox"&gt;&lt;/i&gt; **Dropbox** by opening the &lt;i class="icon-refresh"&gt;&lt;/i&gt; **Synchronize** sub-menu and by clicking **Open from...**. Once opened, any modification in your document will be automatically synchronized with the file in your **Google Drive** / **Dropbox** account.

#### &lt;i class="icon-refresh"&gt;&lt;/i&gt; Save a document

You can save any document by opening the &lt;i class="icon-refresh"&gt;&lt;/i&gt; **Synchronize** sub-menu and by clicking **Save on...**. Even if your document is already synchronized with **Google Drive** or **Dropbox**, you can export it to a another location. StackEdit can synchronize one document with multiple locations and accounts.

#### &lt;i class="icon-refresh"&gt;&lt;/i&gt; Synchronize a document

Once your document is linked to a &lt;i class="icon-provider-gdrive"&gt;&lt;/i&gt; **Google Drive** or a &lt;i class="icon-provider-dropbox"&gt;&lt;/i&gt; **Dropbox** file, StackEdit will periodically (every 3 minutes) synchronize it by downloading/uploading any modification. A merge will be performed if necessary and conflicts will be detected.

If you just have modified your document and you want to force the synchronization, click the &lt;i class="icon-refresh"&gt;&lt;/i&gt; button in the navigation bar.

&gt; **Note:** The &lt;i class="icon-refresh"&gt;&lt;/i&gt; button is disabled when you have no document to synchronize.

#### &lt;i class="icon-refresh"&gt;&lt;/i&gt; Manage document synchronization

Since one document can be synchronized with multiple locations, you can list and manage synchronized locations by clicking &lt;i class="icon-refresh"&gt;&lt;/i&gt; **Manage synchronization** in the &lt;i class="icon-refresh"&gt;&lt;/i&gt; **Synchronize** sub-menu. This will let you remove synchronization locations that are associated to your document.

&gt; **Note:** If you delete the file from **Google Drive** or from **Dropbox**, the document will no longer be synchronized with that location.

----------


Publication
-------------

Once you are happy with your document, you can publish it on different websites directly from StackEdit. As for now, StackEdit can publish on **Blogger**, **Dropbox**, **Gist**, **GitHub**, **Google Drive**, **Tumblr**, **WordPress** and on any SSH server.

#### &lt;i class="icon-upload"&gt;&lt;/i&gt; Publish a document

You can publish your document by opening the &lt;i class="icon-upload"&gt;&lt;/i&gt; **Publish** sub-menu and by choosing a website. In the dialog box, you can choose the publication format:

- Markdown, to publish the Markdown text on a website that can interpret it (**GitHub** for instance),
- HTML, to publish the document converted into HTML (on a blog for example),
- Template, to have a full control of the output.

&gt; **Note:** The default template is a simple webpage wrapping your document in HTML format. You can customize it in the **Advanced** tab of the &lt;i class="icon-cog"&gt;&lt;/i&gt; **Settings** dialog.

#### &lt;i class="icon-upload"&gt;&lt;/i&gt; Update a publication

After publishing, StackEdit will keep your document linked to that publication which makes it easy for you to update it. Once you have modified your document and you want to update your publication, click on the &lt;i class="icon-upload"&gt;&lt;/i&gt; button in the navigation bar.

&gt; **Note:** The &lt;i class="icon-upload"&gt;&lt;/i&gt; button is disabled when your document has not been published yet.

#### &lt;i class="icon-upload"&gt;&lt;/i&gt; Manage document publication

Since one document can be published on multiple locations, you can list and manage publish locations by clicking &lt;i class="icon-upload"&gt;&lt;/i&gt; **Manage publication** in the &lt;i class="icon-provider-stackedit"&gt;&lt;/i&gt; menu panel. This will let you remove publication locations that are associated to your document.

&gt; **Note:** If the file has been removed from the website or the blog, the document will no longer be published on that location.

----------


Markdown Extra
--------------------

StackEdit supports **Markdown Extra**, which extends **Markdown** syntax with some nice features.

&gt; **Tip:** You can disable any **Markdown Extra** feature in the **Extensions** tab of the &lt;i class="icon-cog"&gt;&lt;/i&gt; **Settings** dialog.

&gt; **Note:** You can find more information about **Markdown** syntax [here][2] and **Markdown Extra** extension [here][3].


### Tables

**Markdown Extra** has a special syntax for tables:

Item     | Value
-------- | ---
Computer | $1600
Phone    | $12
Pipe     | $1

You can specify column alignment with one or two colons:

| Item     | Value | Qty   |
| :------- | ----: | :---: |
| Computer | $1600 |  5    |
| Phone    | $12   |  12   |
| Pipe     | $1    |  234  |


### Definition Lists

**Markdown Extra** has a special syntax for definition lists too:

Term 1
Term 2
:   Definition A
:   Definition B

Term 3

:   Definition C

:   Definition D

	&gt; part of definition D


### Fenced code blocks

GitHub's fenced code blocks are also supported with **Highlight.js** syntax highlighting:

```
// Foo
var bar = 0;
```

&gt; **Tip:** To use **Prettify** instead of **Highlight.js**, just configure the **Markdown Extra** extension in the &lt;i class="icon-cog"&gt;&lt;/i&gt; **Settings** dialog.

&gt; **Note:** You can find more information:

&gt; - about **Prettify** syntax highlighting [here][5],
&gt; - about **Highlight.js** syntax highlighting [here][6].


### Footnotes

You can create footnotes like this[^footnote].

  [^footnote]: Here is the *text* of the **footnote**.


### SmartyPants

SmartyPants converts ASCII punctuation characters into "smart" typographic punctuation HTML entities. For example:

|                  | ASCII                        | HTML              |
 ----------------- | ---------------------------- | ------------------
| Single backticks | `'Isn't this fun?'`            | 'Isn't this fun?' |
| Quotes           | `"Isn't this fun?"`            | "Isn't this fun?" |
| Dashes           | `-- is en-dash, --- is em-dash` | -- is en-dash, --- is em-dash |


### Table of contents

You can insert a table of contents using the marker `[TOC]`:

[TOC]


### MathJax

You can render *LaTeX* mathematical expressions using **MathJax**, as on [math.stackexchange.com][1]:

The *Gamma function* satisfying $\Gamma(n) = (n-1)!\quad\forall n\in\mathbb N$ is via the Euler integral

$$
\Gamma(z) = \int_0^\infty t^{z-1}e^{-t}dt\,.
$$

&gt; **Tip:** To make sure mathematical expressions are rendered properly on your website, include **MathJax** into your template:

```
&lt;script type="text/javascript" src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS_HTML"&gt;&lt;/script&gt;
```

&gt; **Note:** You can find more information about **LaTeX** mathematical expressions [here][4].


### UML diagrams

You can also render sequence diagrams like this:

```sequence
Alice-&gt;Bob: Hello Bob, how are you?
Note right of Bob: Bob thinks
Bob--&gt;Alice: I am good thanks!
```

And flow charts like this:

```flow
st=&gt;start: Start
e=&gt;end
op=&gt;operation: My Operation
cond=&gt;condition: Yes or No?

st-&gt;op-&gt;cond
cond(yes)-&gt;e
cond(no)-&gt;op
```

&gt; **Note:** You can find more information:

&gt; - about **Sequence diagrams** syntax [here][7],
&gt; - about **Flow charts** syntax [here][8].

### Support StackEdit

[![](https://cdn.monetizejs.com/resources/button-32.png)](https://monetizejs.com/authorize?client_id=ESTHdCYOi18iLhhO&amp;summary=true)

  [^stackedit]: [StackEdit](https://stackedit.io/) is a full-featured, open-source Markdown editor based on PageDown, the Markdown library used by Stack Overflow and the other Stack Exchange sites.


  [1]: http://math.stackexchange.com/
  [2]: http://daringfireball.net/projects/markdown/syntax "Markdown"
  [3]: https://github.com/jmcmanus/pagedown-extra "Pagedown Extra"
  [4]: http://meta.math.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference
  [5]: https://code.google.com/p/google-code-prettify/
  [6]: http://highlightjs.org/
  [7]: http://bramp.github.io/js-sequence-diagrams/
  [8]: http://adrai.github.io/flowchart.js/
</PRE></BODY></HTML>
