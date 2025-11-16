## Palette

### <code>Palette(<em>colors</em>, <em>names</em>=None)</code>

Create palette.

`colors: dict[int|list[int], int | None]`
: dictionary mapping color values to indices or None

`names: dict[str, int] | None = None`
: optional dictionary mapping names to indices


### <code><em>color</em> in palette</code> -> bool

Check wether `palette` contains the color or name.

`color: str | int | tuple[int, ...] | float | None`
: color or name

### <code>palette[<em>color</em>] -> int | None</code>

Gets index of color or name.

`color: str | int | tuple[int, ...] | float | None`
: color or name

### `len(palette) -> int`

Returns the number of colors contained in palette.

### <code>palette.add_colors(<em>colors</em>)</code>

Add additional color mappings to palette.

`colors: dict[int|list[int], int | None]`
: colors to add

### <code>palette.add_names(<em>names</em>)</code>

Add additional names to palette.

`names: dict[str, int]`
: names to add

### `palette.bit_length() -> int`

Get the number of bits required to represent any index.

### <code>palette.get_colors(<em>index</em>) -> list[int]</code>

Get all colors matching to given index or name.

`index: str | int`
: index or name

### <code>palette.get_index(<em>name</em>) -> int</code>

Get index of name.

`name: str`
: name
