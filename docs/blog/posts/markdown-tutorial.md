---
date: 2023-08-13
authors:
  - Jake
categories:
  - Guide
  - Beginner
tags:
  - markdown
comments: true
---

# Learn markdown in 10 minutes!

[:material-language-markdown: Markdown](https://en.wikipedia.org/wiki/Markdown) is a simple markup language that allows you to write formatted text using a plain-text editor. It is a popular choice for writing documentation, blog posts, forum posts, and other content that is published online. If you don't know markdown already, this tutorial will teach you the basics.
<!-- more -->
Markdown files end with `.md` or `.markdown` extension, and are rendered with a markdown processor. The most popular markdown processor is [CommonMark](https://commonmark.org/).

## A brief history of markdown

Markdown was initially developed by John Gruber (with help from Aaron Swartz) in 2004. It was designed to be as readable and easy-to-write as possible, while being able to be converted to valid HTML.

Markdown is now one of the most popular markup languages, and is used by many websites, including GitHub, Reddit, Stack Overflow, and more.

## Markdown syntax

This guide will cover the basic markdown syntax which is supported by most markdown processors. I will use [CommonMark specification](https://spec.commonmark.org/) as the reference. Let's get started!

### Text formatting

Surround the text with `*` or `_` to emphasize the text. This is the syntax:

``` markdown
*This text is italic*
**And, this text is bold**

Or you can use underscores instead:

_This text is also italic_
__And, this text is also bold__
```

It's pretty straightforward. Here are some more examples:

| Markdown | Rendered output |
| -------- | --------------- |
| `Markdown is **fun!**` |  Markdown is **fun!** |
| `Dumbledore said _calmly_.` |  Dumbledore said _calmly_. |
| `Super*cali*fragilistc...` |  Super*cali*fragilistc... |
| `...**expi**alidocious` | ...**expi**alidocious |
| `***Very important!***` | **_Very important!_** |

!!! success "Best practice"
    For the best compatibility, use `*` instead of `_` for emphasis.

### Paragraphs

Paragraphs are separated by a blank line. For example:

``` markdown
This is the first paragraph.

And this is the second one.
I'm still on paragraph two, by the way.

And this is the third paragraph.
```

??? tip "Adding a line break"
    You can add a line break by adding two spaces or a backslash `\` at the end of the line. For example:

    ``` markdown
    This is the first line.\
    And this is the second line.
    ```

### Headings

Headings begin with a `#` and a space. You can use multiple `#` to change the level of the heading. The more the `#`, the smaller the heading. The level of heading corresponds to the HTML heading element as follows:

```markdown
# This is an <h1>
## This is an <h2>
### This is an <h3>
#### This is an <h4>
##### This is an <h5>
###### This is an <h6>
```

You can also alternatively use this syntax to represent h1 and h2 headings:

```markdown
This is an <h1>
===============

This is an <h2>
---------------
```

You can use formatting (emphasis, links, etc.) in headings, too.

!!! success "Best practice"
    Add a line before and after headings to make them readable.

### Blockquotes

Blockquotes are used to quote text from another source. Use `>` at the beginning of the line to create a blockquote. You can also nest blockquotes by adding additional `>`.

``` markdown
> This is a blockquote.
> It can span multiple lines.
>
> It can span multiple paragraphs, too.
> > This is a nested blockquote!
> > > **Wow!**
```

??? abstract "See output"
    > This is a blockquote.
    > It can span multiple lines.
    >
    > It can span multiple paragraphs, too.
    > > This is a nested blockquote!
    > > > **Wow!**

!!! success "Best practice"
    The space after `>` is not required, but it makes the markdown more readable.

### Lists

Unordered lists can be created by using `*`, `-`, or `+` at the beginning of the line. For example:

``` markdown
* Caspar
* Balthazar
* Melchior
```

A space is required after the list marker.

??? abstract "See output"
    + Caspar
    + Balthazar
    + Melchior

We can also nest lists. Nesting can be done by indenting the list marker. For example:

``` markdown
* Caspar
  * name of the friendly ghost
  * name of the Guru of Time in *Chrono Trigger*
* Melchior
```

??? abstract "See output"
    + Caspar
        - name of the friendly ghost
        - name of the Guru of Time in *Chrono Trigger*
    + Melchior

Ordered lists can be created by using numbers followed by a period `.` or a right parenthesis `)` at the beginning of the line. For example:

``` markdown
1. Caspar
2. Balthazar
3. Melchior
```

??? abstract "See output"
    1. Caspar
    2. Balthazar
    3. Melchior

If you start the list with a number other than 1, the numbers will be incremented accordingly. Also, you don't have to write the numbers in order, only the first number matters.

### Links

Links can be created by using this syntax: `[link text](url)`. For example:

``` markdown
[I am a *link*!](https://w.wiki/7FBk).

Click [here](https://archive.org/) to visit the Internet Archive.
```

??? abstract "See output"
    [I am a _link_!](https://w.wiki/7FBk).

    Click [here](https://archive.org/) to visit the Internet Archive.

??? tip "Adding a title to links"
    Link title is displayed when you hover over the link.

    Adding a title is as easy as adding a space after the URL and enclosing the title in quotes. For example:

    ``` markdown
    [I am a *link*!](https://w.wiki/7FBk "This is the link title.")
    ```

#### Reference-style links

You can also use reference-style links. This is useful when you want to link to the same URL multiple times. This is how it works:

``` markdown
[Take me home!][homepage]
Also, my social media accounts are listed [here][homepage].

[homepage]: https://jake.is-a.dev/ "This is the link title."
```

`homepage` is the link reference. It can consist of letters, numbers, spaces and punctuation. It's not case-sensitive.

The last line is the link definition. It consists of the link reference, followed by a colon `:`, followed by the URL. The optional title can be added by adding a space and enclosing the title in quotes.

The link definition can be placed anywhere after a blank line, but it's usually placed at the end of the document.

### Images

Images are similar to links, but they start with an exclamation mark `!`. Its syntax is `![alt text](url)`. For example:

``` markdown
![A cute kitten](https://placekitten.com/200/200)
```

??? abstract "See output"
    ![A cute kitten](https://placekitten.com/200/200)

??? question "What is alt text?"
    Alt text is used to describe the image. It is displayed when the image fails to load. It is also used by screen readers to describe the image to visually impaired users.

??? tip "Adding a title to images"
    Adding a title to images is similar to adding a title to links. Add a space after the URL and enclose the title in quotes. For example:

    ``` markdown
    ![A cute kitten](https://placekitten.com/200/200 "This is the image title.")
    ```

#### Reference-style images

[Just like links](#reference-style-links), you can also use reference-style images. Just add a `!` at the beginning of the link reference. Nothing else changes.

### Code

Inline code can be created by surrounding the text with backticks `` ` ``. For example:

``` markdown
The `printf()` function is used to print text. This function is imported from the `stdio.h` header file.
```

??? abstract "See output"
    The `printf()` function is used to print text. This function is imported from the `stdio.h` header file.

#### Code blocks

Code blocks (or fences) are used to display a block of code (duh!). Code blocks can be created by indenting the code by four spaces or one tab. For example:

``` markdown
    import os

    while True:
        os.fork()
```

??? abstract "See output"
        import os

        while True:
            os.fork()

You can also use triple backticks `` ``` `` to create code blocks. For example:

    ```
        import os

        while True:
            os.fork()
    ```

### Horizontal rules

Horizontal rules can be created by placing three or more `*`, `-`, or `_` on a blank line. For example:
  
``` markdown
Hello, world!
***
There's a line above me! That's the horizontal rule.
```

??? abstract "See output"
    Hello, world!
    ***
    There's a line above me! That's the horizontal rule.

### More markdown

Congratulations! You've covered the basics of markdown. But that's not all. Let's learn about some nice features of markdown. All of this is supported by most markdown processors.

#### HTML tags

Most inline HTML tags are supported, meaning markdown is a superset of HTML (not necessarily, though). This means you can use HTML tags in markdown, but it isn't recommended.

``` markdown
Using a <abbr title="Virtual Private Network">VPN</abbr> will shift your trust from your <abbr title="Internet Service Provider">ISP</abbr> to your VPN provider.
```

You cannot use markdown syntax inside HTML tags in most markdown processors.

??? abstract "See output"
    Using a <abbr title="Virtual Private Network">VPN</abbr> will shift your trust from your <abbr title="Internet Service Provider">ISP</abbr> to your VPN provider.

!!! success "Best practice"
    For the best compatibility, avoid using HTML tags in markdown. Some markdown processors doesn't support all HTML tags.

#### Automatic links

URLs and emails can be converted to links automatically if you enclose them in angle brackets `<` and `>`. For example:

``` markdown
<https://neal.fun/> is a cool website.

Email me your favorite websites at <email@example.com>.
```

??? abstract "See output"
    <https://neal.fun/> is a cool website.

    Email me your favorite websites at <email@example.com>.

#### Escaping characters

Sometimes, you may want to use characters that are reserved by markdown. You can escape these characters by adding a backslash `\` before the character. For example:

``` markdown
\*This is not italic\*

\# This is not a heading

All classes have a \__init__() function in Python.
```

??? abstract "See output"
    \*This is not italic\*

    \# This is not a heading

    All classes have a \__init__() function in Python.

## Extended syntax

!!! question "Did you know?"
    This blog post is written in markdown! Check out the [source code](https://github.com/j-eo/website/blob/main/docs/blog/posts/markdown-tutorial.md?plain=1) to see how it's done. You may not understand everything, because it uses extensions to the markdown syntax.

The CommonMark syntax was not enough for some people, so they extended the syntax to add more features. Let's learn about some of them.

### GitHub Flavored Markdown

GitHub Flavored Markdown (GFM) is a superset of CommonMark. It adds some features that are useful for writing documentation, like tables, task lists, strikethrough, etc. If you use GitHub  The complete specification can be found [here](https://github.github.com/gfm/).

### Markdown Extra

Markdown Extra supports features like markdown support inside HTML blocks, footnotes, abbreviations, definition lists, fenced code blocks, etc. Learn more about it [here](https://michelf.ca/projects/php-markdown/extra/).

## That's about it

That's all you need to know to get started with markdown. Now, you can write `README.md` files for your GitHub repositories, write blog posts, and more!
