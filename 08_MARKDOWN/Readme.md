# MARKDOWN

Markdown is an easy-to-read, easy-to-write language for formatting plain text. You can use Markdown syntax, along with some additional HTML tags, to format your writing on GitHub, in places like repository READMEs and comments on pull requests and issues.

## Markup 
A Markup language is a way of formatting and presenting text data in a different format.

A common use-case for markup language is to present data in HTML.

## Markdown

Markdown is a markup language that provides a shorthand syntax to format information into HTML. Markdown is popular due to easy syntax, and being readable in its raw format.

> [!CAUTION]  
> Do not confuse markup language with markdown:
> - Markup is a general term referring to the process of adding tags to format a document
> - Markdown is a specific lightweight markup language that simplifies this process and is used for creating content on various platforms in a straightforward manner.

Markdown extensions are `.md` and `.markdown`.

The general concept is:
> We write in **Markdown** -> Its transform into HMTL -> An HTML preview is generated

## Markdown basic and extended syntax

All markdown parsers support the following markdown syntax:

### Headings

To create a heading, add one to six <kbd>#</kbd> symbols before your heading text. The number of <kbd>#</kbd> you use will determine the hierarchy level and typeface size of the heading.

```md
# A first-level heading
## A second-level heading
### A third-level heading
```

> [!TIP]
> With headings GitHub automatically generates a table of contents that you can access. Each heading title is listed in the table of contents and you can click a title to navigate to the selected section.


### Styling text

You can indicate emphasis with bold, italic, strikethrough, subscript, or superscript text in comment fields and `.md` files.

| Style | Syntax | Example | Output |
| --- | --- | --- | --- | 
| Bold | ** ** or __ __ | `**This is bold text**` |	**This is bold text** |
| Italic | * * or _ _ |	`*This text is italicized*` |	*This is bold text* |
| Strikethrough | ~~  ~~ | `~~This was mistaken text~~` |	~~This was mistaken text~~ |
| Bold and nested italic | ** ** and _ _ |	`**This text is _extremely_ important**` | **This text is _extremely_ important** |
| All bold and italic | *** *** | `***All this text is important***` | ***All this text is important*** |
| Subscript | <sub> </sub> | `This is a <sub>subscript</sub> text` | This is a <sub>subscript</sub> text |
| Superscript | <sup> </sup> | `This is a <sup>superscript</sup> text` | This is a <sup>superscript</sup> text |


### Quoting text or blockquote

You can quote text with a <kbd>></kbd> for example `> Text that is a quote`

> Text that is a quote

### Quoting code inline

You can call out code or a command within a sentence with single backticks <kbd>`</kbd> at the start and the end.

`For example this is inline-code`


### Quoting code block
To start and the block put 3 <kbd>`</kbd> together.

```
This is a block code
```

> [!IMPORTANT]  
> By writting the extension file in the first 3 <kbd>`</kbd> the bloc its colored if code mach the extension file.

```py
print("This it python code" )
```

### Links

You can create an inline link by wrapping link text in brackets <kbd>[ ]</kbd>, and then wrapping the URL in parentheses <kbd>( )</kbd>, it will look like this [GitHub Docs](https://docs.github.com/)

`This repo was built using [GitHub Docs](https://docs.github.com/).`

### Relative links

You can define relative links and image paths in your rendered files to help readers navigate to other files in your repository.

The path of the link will be relative to the current file. Links starting with <kbd>/</kbd> will be relative to the repository root. You can use all relative link operands, such as <kbd>./</kbd> and <kbd>../</kbd>.

For example [Readme of this repo](README.md), the syntax is `[Readme of this repo](README.md)`


### Images

To use a image its very similar to a link, just add <kbd>!</kbd> at the start

The syntax is `![Github foundation logo](https://github.com/Andresmup/github-foundations/blob/dev/images/GithubFundationBadget.png?raw=true)`


### Horizontal Ruler

A quick and easy way organize and separe sections of is using `---`, this generate a line in the file.

---