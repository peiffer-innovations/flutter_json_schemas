[*description*][description]

# MaterialType enum #

The various kinds of material in material design. Used to configure the default behavior of Material widgets.

See also:

 *  Material, in particular Material.type.
 *  kMaterialEdges

## Constants ##

button → const MaterialType

Rounded edges, no color by default (used for MaterialButton buttons).

`const MaterialType(3)`

canvas → const MaterialType

Rectangle using default theme canvas color.

`const MaterialType(0)`

card → const MaterialType

Rounded edges, card theme color.

`const MaterialType(1)`

circle → const MaterialType

A circle, no color by default (used for floating action buttons).

`const MaterialType(2)`

transparency → const MaterialType

A transparent piece of material that draws ink splashes and highlights.

While the material metaphor describes child widgets as printed on the material itself and do not hide ink effects, in practice the Material widget draws child widgets on top of the ink effects. A Material with type transparency can be placed on top of opaque widgets to show ink effects on top of them.

Prefer using the Ink widget for showing ink effects on top of opaque widgets.

`const MaterialType(4)`

values → const List<MaterialType>

A constant List of the values in this enum, in order of their declaration.

`const List<MaterialType>`

## Properties ##

hashCode → int

The hash code for this object. \[...\]

read-only, inherited

index → int

The integer index of this enum.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

toString() → String

Returns a string representation of this object.

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/material.dart#L27