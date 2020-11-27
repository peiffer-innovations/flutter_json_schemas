[*description*][description]

# ImageRepeat enum Null safety #

How to paint any portions of a box not covered by an image.

## Constants ##

noRepeat → const ImageRepeat

Leave uncovered portions of the box transparent.

`const ImageRepeat(3)`

repeat → const ImageRepeat

Repeat the image in both the x and y directions until the box is filled.

`const ImageRepeat(0)`

repeatX → const ImageRepeat

Repeat the image in the x direction until the box is filled horizontally.

`const ImageRepeat(1)`

repeatY → const ImageRepeat

Repeat the image in the y direction until the box is filled vertically.

`const ImageRepeat(2)`

values → const List<ImageRepeat>

A constant List of the values in this enum, in order of their declaration.

`const List<ImageRepeat>`

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/painting/decoration_image.dart#L21