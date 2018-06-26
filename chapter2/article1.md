# MacDown

![MacDown logo](http://macdown.uranusjr.com/static/images/logo-160.png)

Hello there! I’m **MacDown**, the open source Markdown editor for OS X.

Let me introduce myself.



## Markdown and I

**Markdown** is a plain text formatting syntax created by John Gruber, aiming to provide a easy-to-read and feasible markup. The original Markdown syntax specification can be found [here](http://daringfireball.net/projects/markdown/syntax).

**MacDown** is created as a simple-to-use editor for Markdown documents. I render your Markdown contents real-time into HTML, and display them in a preview panel.

![MacDown Screenshot](http://d.pr/i/10UGP+)

I support all the original Markdown syntaxes. But I can do so much more! Various popular but non-standard syntaxes can be turned on/off from the [**Markdown** preference pane](#markdown-pane).

You can specify extra HTML rendering options through the [**Rendering** preference pane](#rendering-pane).

You can customize the editor window to you liking in the [**Editor** preferences pane](#editor-pane):

You can configure various application (that's me!) behaviors in the [**General** preference pane](#general-pane).

## The Basics
Before I tell you about all the extra syntaxes and capabilities I have, I'll introduce you to the basics of standard markdown. If you already know markdown, and want to jump straight to learning about the fancier things I can do, I suggest you skip to the [**Markdown** preference pane](#markdown-pane). Lets jump right in.  

### Line Breaks
To force a line break, put two spaces and a newline (return) at the end of the line.

* This two-line bullet
won't break

* This two-line bullet  
will break

Here is the code:

```
* This two-line bullet
won't break

* This two-line bullet  
will break
```

### Strong and Emphasize

**Strong**: `**Strong**` or `__Strong__` (Command-B)  
*Emphasize*: `*Emphasize*` or `_Emphasize_`[^emphasize] (Command-I)

### Headers (like this one!)

	Header 1
	========

	Header 2
	--------

or

	# Header 1
	## Header 2
	### Header 3
	#### Header 4
	##### Header 5
	###### Header 6



### Links and Email
#### Inline
Just put angle brackets around an email and it becomes clickable: <uranusjr@gmail.com>  
`<uranusjr@gmail.com>`  

Same thing with urls: <http://macdown.uranusjr.com>  
` <http://macdown.uranusjr.com>`  

Perhaps you want to some link text like this: [Macdown Website](http://macdown.uranusjr.com "Title")  
`[Macdown Website](http://macdown.uranusjr.com "Title")` (The title is optional)  


#### Reference style
Sometimes it looks too messy to include big long urls inline, or you want to keep all your urls together.  

Make [a link][arbitrary_id] `[a link][arbitrary_id]` then on it's own line anywhere else in the file:  
`[arbitrary_id]: http://macdown.uranusjr.com "Title"`

If the link text itself would make a good id, you can link [like this][] `[like this][]`, then on it's own line anywhere else in the file:  
`[like this]: http://macdown.uranusjr.com`  

[arbitrary_id]: http://macdown.uranusjr.com "Title"
[like this]: http://macdown.uranusjr.com  


### Images
#### Inline
`![Alt Image Text](path/or/url/to.jpg "Optional Title")`
#### Reference style
`![Alt Image Text][image-id]`  
on it's own line elsewhere:  
`[image-id]: path/or/url/to.jpg "Optional Title"`


### Lists

* Lists must be preceded by a blank line (or block element)
* Unordered lists start each item with a `*`
- `-` works too
	* Indent a level to make a nested list
		1. Ordered lists are supported.
		2. Start each item (number-period-space) like `1. `
		42. It doesn't matter what number you use, I will render them sequentially
		1. So you might want to start each line with `1.` and let me sort it out

Here is the code:

```
* Lists must be preceded by a blank line (or block element)
* Unordered lists start each item with a `*`
- `-` works too
	* Indent a level to make a nested list
		1. Ordered lists are supported.
		2. Start each item (number-period-space) like `1. `
		42. It doesn't matter what number you use, I will render them sequentially
		1. So you might want to start each line with `1.` and let me sort it out
```



### Block Quote

> Angle brackets `>` are used for block quotes.  
Technically not every line needs to start with a `>` as long as
there are no empty lines between paragraphs.  
> Looks kinda ugly though.
> > Block quotes can be nested.  
> > > Multiple Levels
>
> Most markdown syntaxes work inside block quotes.
>
> * Lists
> * [Links][arbitrary_id]
> * Etc.

Here is the code:

```
> Angle brackets `>` are used for block quotes.  
Technically not every line needs to start with a `>` as long as
there are no empty lines between paragraphs.  
> Looks kinda ugly though.
> > Block quotes can be nested.  
> > > Multiple Levels
>
> Most markdown syntaxes work inside block quotes.
>
> * Lists
> * [Links][arbitrary_id]
> * Etc.
```


### Inline Code
`Inline code` is indicated by surrounding it with backticks:  
`` `Inline code` ``

If your ``code has `backticks` `` that need to be displayed, you can use double backticks:  
```` ``Code with `backticks` `` ````  (mind the spaces preceding the final set of backticks)


### Block Code
If you indent at least four spaces or one tab, I'll display a code block.

	print('This is a code block')
	print('The block must be preceded by a blank line')
	print('Then indent at least 4 spaces or 1 tab')
		print('Nesting does nothing. Your code is displayed Literally')

I also know how to do something called [Fenced Code Blocks](#fenced-code-block) which I will tell you about later.

### Horizontal Rules
If you type three asterisks `***` or three dashes `---` on a line, I'll display a horizontal rule:

***


### Styling

My editor provides syntax highlighting. You can edit the base font and the coloring/sizing theme. I provided some default themes (courtesy of [Mou](http://mouapp.com)’s creator, Chen Luo) if you don’t know where to start.

You can also edit, or even add new themes if you want to! Just click the ***Reveal*** button, and start moving things around. Remember to use the correct file extension (`.styles`), though. I’m picky about that.

I offer auto-completion and other functions to ease your editing experience. If you don’t like it, however, you can turn them off.





## Hack On

That’s about it. Thanks for listening. I’ll be quiet from now on (unless there’s an update about the app—I’ll remind you for that!).

Happy writing!


[^emphasize]: If **Underlines** is turned on, `_this notation_` will render as underlined instead of emphasized

[^under]: If **Underline** is disabled `_this_` will be rendered as *emphasized* instead of being underlined.

[^quote]: **Quote** replaces literal `"` characters with html `<q>` tags. **Quote** and **Smartypants** are syntactically incompatible. If both are enabled, **Quote** takes precedence. Note that **Quote** is different from *blockquote*, which is part of standard Markdown.

[^math]: Internet connection required.
