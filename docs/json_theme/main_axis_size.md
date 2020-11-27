[*description*][description]

# MainAxisSize enum Null safety #

How much space should be occupied in the main axis.

During a flex layout, available space along the main axis is allocated to children. After allocating space, there might be some remaining free space. This value controls whether to maximize or minimize the amount of free space, subject to the incoming layout constraints.

See also:

 *  Column, Row, and Flex, the flex widgets.
 *  Expanded and Flexible, the widgets that controls a flex widgets' children's flex.
 *  RenderFlex, the flex render object.
 *  MainAxisAlignment, which controls how the free space is distributed.

## Constants ##

max → const MainAxisSize

Maximize the amount of free space along the main axis, subject to the incoming layout constraints.

If the incoming layout constraints have a small enough BoxConstraints.maxWidth or BoxConstraints.maxHeight, there might still be no free space.

If the incoming layout constraints are unbounded, the RenderFlex will assert, because there would be infinite remaining free space and boxes cannot be given infinite size.

`const MainAxisSize(1)`

min → const MainAxisSize

Minimize the amount of free space along the main axis, subject to the incoming layout constraints.

If the incoming layout constraints have a large enough BoxConstraints.minWidth or BoxConstraints.minHeight, there might still be a non-zero amount of free space.

If the incoming layout constraints are unbounded, and any children have a non-zero FlexParentData.flex and a FlexFit.tight fit (as applied by Expanded), the RenderFlex will assert, because there would be infinite remaining free space and boxes cannot be given infinite size.

`const MainAxisSize(0)`

values → const List<MainAxisSize>

A constant List of the values in this enum, in order of their declaration.

`const List<MainAxisSize>`

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/rendering/flex.dart#L71