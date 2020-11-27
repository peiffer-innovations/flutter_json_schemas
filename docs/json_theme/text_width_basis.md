[*description*][description]

# TextWidthBasis enum Null safety #

The different ways of measuring the width of one or more lines of text.

See Text.textWidthBasis, for example.

## Constants ##

longestLine → const TextWidthBasis

The width will be exactly enough to contain the longest line and no longer. A common use case for this is chat bubbles.

`const TextWidthBasis(1)`

parent → const TextWidthBasis

multiline text will take up the full width given by the parent. For single line text, only the minimum amount of width needed to contain the text will be used. A common use case for this is a standard series of paragraphs.

`const TextWidthBasis(0)`

values → const List<TextWidthBasis>

A constant List of the values in this enum, in order of their declaration.

`const List<TextWidthBasis>`

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/painting/text_painter.dart#L87