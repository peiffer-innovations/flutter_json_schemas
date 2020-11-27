[*description*][description]

# FlexFit enum Null safety #

How the child is inscribed into the available space.

See also:

 *  RenderFlex, the flex render object.
 *  Column, Row, and Flex, the flex widgets.
 *  Expanded, the widget equivalent of tight.
 *  Flexible, the widget equivalent of loose.

## Constants ##

loose → const FlexFit

The child can be at most as large as the available space (but is allowed to be smaller).

The Flexible widget assigns this kind of FlexFit to its child.

`const FlexFit(1)`

tight → const FlexFit

The child is forced to fill the available space.

The Expanded widget assigns this kind of FlexFit to its child.

`const FlexFit(0)`

values → const List<FlexFit>

A constant List of the values in this enum, in order of their declaration.

`const List<FlexFit>`

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/rendering/flex.dart#L21