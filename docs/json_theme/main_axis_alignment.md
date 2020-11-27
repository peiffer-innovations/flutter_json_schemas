[*description*][description]

# MainAxisAlignment enum Null safety #

How the children should be placed along the main axis in a flex layout.

See also:

 *  Column, Row, and Flex, the flex widgets.
 *  RenderFlex, the flex render object.

## Constants ##

center → const MainAxisAlignment

Place the children as close to the middle of the main axis as possible.

`const MainAxisAlignment(2)`

end → const MainAxisAlignment

Place the children as close to the end of the main axis as possible.

If this value is used in a horizontal direction, a TextDirection must be available to determine if the end is the left or the right.

If this value is used in a vertical direction, a VerticalDirection must be available to determine if the end is the top or the bottom.

`const MainAxisAlignment(1)`

spaceAround → const MainAxisAlignment

Place the free space evenly between the children as well as half of that space before and after the first and last child.

`const MainAxisAlignment(4)`

spaceBetween → const MainAxisAlignment

Place the free space evenly between the children.

`const MainAxisAlignment(3)`

spaceEvenly → const MainAxisAlignment

Place the free space evenly between the children as well as before and after the first and last child.

`const MainAxisAlignment(5)`

start → const MainAxisAlignment

Place the children as close to the start of the main axis as possible.

If this value is used in a horizontal direction, a TextDirection must be available to determine if the start is the left or the right.

If this value is used in a vertical direction, a VerticalDirection must be available to determine if the start is the top or the bottom.

`const MainAxisAlignment(0)`

values → const List<MainAxisAlignment>

A constant List of the values in this enum, in order of their declaration.

`const List<MainAxisAlignment>`

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/rendering/flex.dart#L104