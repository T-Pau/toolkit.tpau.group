---
layout: page
title: parallel-struct
---
### Create parallel tables from list of structures.

## Synopsis

```sh
parallel-struct [-M file] [-o file] [-I directory] [-s section] structs
```

## Description

Create tables for each field in a list of structures.

It generates an assembler source file containing all the created objects.


## Supported Options

`-h`, `--help`
:   Show help message and exit.

<code>-M <em>file</em><code>
: Write gcc-style dependency information to `file`.

<code>-o <em>file</em></code>
:   Write generated assembly code to `file`.

<code>-s <em>section</em></code>, <code>--section <em>section</em></code>
:   Put generated objects in section `section`.


## Structue File

The structures file uses [YAML](https://yaml.org) syntax.

### Settings

Global settings are specified in the `settings` section of the structure file.

<code>default_string_encoding <em>encoding</em></code>
: The default encoding used for string values. (default: `default_string_encoding`)

`include_count {yes|no}`
: (default: `yes`)

<code>prefix </em>string</em></code>
: Prefix for object names. (default: empty)

### Fields

The fields of the structures are defined in the `fields` section of the structure file.

<code>default_value <em>value</em></code>
: Value to use if not specified in struct.

<code>default_value_field <em>field</em></code>
: If set, the default value will be taken from the named field. (default: none)

<code>default_value_prefix <em>string</em></code>
: If `default_value_field` is used, prepend `string` to its value. (default: empty)

<code>default_value_postfix <em>string</em></code>
: If `default_value_field` is used, append `string` to its value. (default: empty)

<code>encoding <em>encoding</em></code>
: Encoding used for string values. (default: `default_string_encoding` from global settings)

<code>length <em>number</em></code>
: (default: 1)

`nul_terminate {yes|no}`
: If set, a NUL character will be appended to string values. (default: `no`)

<code>padding <em>padding</em></code>
: (default: ` ` for string fields, 0 for others.)

<code>type <em>type</em></code>
: (default: `single`)

    `multi`
    :

    `omit`
    :

    `single`
    :

    `string`
    :

### Structures

The actual structures are listed in the `structs` section of the structure file.
