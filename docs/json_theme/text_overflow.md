[*description*][description]

# TextOverflow enum Null safety #

How overflowing text should be handled.

A TextOverflow can be passed to Text and RichText via their Text.overflow and RichText.overflow properties respectively.

## Constants ##

clip → const TextOverflow

Clip the overflowing text to fix its container.

`const TextOverflow(0)`

ellipsis → const TextOverflow

Use an ellipsis to indicate that the text has overflowed.

`const TextOverflow(2)`

fade → const TextOverflow

Fade the overflowing text to transparent.

`const TextOverflow(1)`

values → const List<TextOverflow>

A constant List of the values in this enum, in order of their declaration.

`const List<TextOverflow>`

visible → const TextOverflow

Render overflowing text outside of its container.

`const TextOverflow(3)`

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/rendering/paragraph.dart#L25