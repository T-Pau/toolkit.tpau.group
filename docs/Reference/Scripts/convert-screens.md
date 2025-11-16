---
layout: page
title: convert-screens
---
### Convert text to screens.

## Synopsis

```sh
convert-screens [-M file] [-o file] [-I directory] [-s section] [-D defines] file
```

## Description

Convert text into screens. It allows arbitrary mapping of Unicode characters to screen codes and word wrapping.

It generates an assembler source file containing all the created objects.


## Supported Options

`-h`, `--help`
:   Show help message and exit.

<code>-I <em>directory</em></code>
:   Search for included files in `directory`. Can be given multiple times.

<code>-M <em>file</em><code>
: Write gcc-style dependency information to `file`.

<code>-o <em>file</em></code>
:   Write generated assembly code to `file`.

<code>-s <em>section</em></code>, <code>--section <em>section</em></code>
:   Put generated objects in section `section`.

<code>-D <em>defines>
:   Specify defines.

## Text File

The text file starts with a preamble, specifying how the conversion should be done, followed by pages of text to be converted.

### Preamble

<code>image_padding_left <em>string</em></code>
: (default: empty)

<code>image_padding_right <em>string</em></code>
: (default: empty)

<code>line_length <em>number</em></code>
: (default: 40)

<code>line_skip <em>number</em></code>
: (default: 0)

<code>lines <em>number</em></code>
: (default: 25)

<code>map <em>from</em>[-<em>to</em>] <em>target</em></code>
:

<code>name <em>string</em></code>
: (required)

<code>page_mode <em>mode</em></code>
: (default: `pages`)

    `objects`
    : Create a separate named object for each page.

    `pages`
    : Create an index object containing pointers to each page.

    `single`
    : Create a single page object.

<code>prefix <em>string</em></code>
: (default: empty)

<code>postfix <em>string</em></code>
: (default: empty)

`runlength_encode {yes|no}`
: Runlength encode screen objects. (default: `yes`)

<code>title_length <em>number</em></code>
: (default: 0)

<code>title_xor <em>number</em></code>
: (default: 0)

`word_wrap {yes|no}`
: Automatically word wrap lines to fit into `line_length`. (default: `no`)


