---
layout: page
title: convert-bitmaps
---

## Specification File

The specification file uses [YAML](https://yaml.org) syntax.


### Global Directives

`bitmaps`
: List of [bitmap definitions](#bitmap_directives) describing the images to convert. (required)

`runlength-encode yes|no`
: Wether to runlength encode components (default: `yes`)

<code>section <em>name</em></code>
: Section to place created objects in. (default: `data`)

<code>screen_width <em>number</em></code>
: Specify the default width of the screen. (default: none)

### Bitmap Directives

`components`
: Map of [component definitions](#component_directives) describing each component.

<code>file <em>name</em></code>
: name of image file (required)

<code>name <em>name</em></code>
: Name prefix for default name of component objects.

<code>layout <em>layout</em></code>
: Layout to convert to. (required)

    `c64-hires`
    : Commodore 64 hires bitmap:
        : `screen`
        screen

    `c64-multicolor`
    : Commodore 64 multicolor bitmap:
        : `screen`
        screen

        : `color`
        color ram

        : `background`
        background color

    `zx-spectrum`
    : ZX Spectrum bitmap:
        : `attributes`
        attributes

`runlength-encode yes|no`
: Wether to runlength encode components (default: global `runlength-encode`)

<code>section <em>name</em></code>
: Section to place object into. (default: global `section`)

<code>unused-colors <em>colors</em></code>
: (default: none)

### Component Directives

<code>alignment <em>number</em></code>
: align object to `number`. (default: none)

<code>name <em>name</em></code>
: name of created object (default: <code><em>bitmap-name</em>_<em>component-name</em></code>)

<code>object-type <em>type</em></code>
: type of object to create. (default: `symbol`)

    `constant`
    : constant definition

    `symbol`
    : data symbol

    `omit`
    : don't create any object.

`runlength-encode yes|no`
: Wether to runlength encode components (default: bitmap `runlength-encode`)

<code>section <em>name</em></code>
: section to put object into. (default: bitmap `section`)
