[*description*][description]

# VerticalDirection enum Null safety #

A direction in which boxes flow vertically.

This is used by the flex algorithm (e.g. Column) to decide in which direction to draw boxes.

This is also used to disambiguate `start` and `end` values (e.g. MainAxisAlignment.start or CrossAxisAlignment.end).

See also:

 *  TextDirection, which controls the same thing but horizontally.

## Constants ##

down → const VerticalDirection

Boxes should start at the top and be stacked vertically towards the bottom.

The "start" is at the top, the "end" is at the bottom.

`const VerticalDirection(1)`

up → const VerticalDirection

Boxes should start at the bottom and be stacked vertically towards the top.

The "start" is at the bottom, the "end" is at the top.

`const VerticalDirection(0)`

values → const List<VerticalDirection>

A constant List of the values in this enum, in order of their declaration.

`const List<VerticalDirection>`

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/painting/basic_types.dart#L158