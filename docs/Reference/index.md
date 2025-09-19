<<<<<<< HEAD
# Reference

## [Assembler Source File](Assembler-Source-File.md)

A source file contains definitions that will be translated to a **library** or a **binary program**.

It consists of a list of elements and directives, separated by newlines. Instructions, labels, and assignments within an **object** or **macro** are also separated by newlines.


## [Expressions](Expressions.md)

Expressions are used in various places in a program.


## Library

A library is a collection of **objects**, **constants**, **macros**, and **functions**. 

When importing a library, only the objects actually used will be included in the resulting binary program. This gives you flexibility in how you organize your code: even using only a small portion of a large library does not sacrifice efficiency.


## [Target Definition](Target-Definition.md)

A **target definition** defines the memory layout and binary file format. It supports all the directives of [assembler source files](Assembler-Source-File.md) and a few additional directives.


## [CPU Definition](CPU-Definition.md)

A **CPU definition** defines the syntax of the assembly instructions and how they are encoded.
=======
---
layout: page
title: Reference
---
## Scripts

- [`convert-bitmap` — Convert bitmap image to native format.](convert-bitmap.md)
- [`convert-characters` — Convert images to charset and screens.](convert-charset.md)
- [`convert-charset` — ](convert-charset.md)
- [`convert-image` — ](convert-image.md)
- [`convert-markdown` — ](convert-markdown.md)
- [`convert-screens` — ](convert-screens.md)
- [`convert-sprites` — ](convert-sprites.md)
- [`create-disk` — ](create-disk.md)
- [`create-zip` — ](create-zip.md)
- [`encode-colors` — ](encode-colors.md)
- [`parallel-struct` — ](parallel-struct.md)
>>>>>>> bd0a15b (Flesh out.)
