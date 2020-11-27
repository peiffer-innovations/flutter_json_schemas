[*description*][description]

# BoxShape enum Null safety #

The shape to use when rendering a Border or BoxDecoration.

Consider using ShapeBorder subclasses directly (with ShapeDecoration), instead of using BoxShape and Border, if the shapes will need to be interpolated or animated. The Border class cannot interpolate between different shapes.

## Constants ##

circle → const BoxShape

A circle centered in the middle of the box into which the Border or BoxDecoration is painted. The diameter of the circle is the shortest dimension of the box, either the width or the height, such that the circle touches the edges of the box.

See also:

 *  CircleBorder, the equivalent ShapeBorder.

`const BoxShape(1)`

rectangle → const BoxShape

An axis-aligned, 2D rectangle. May have rounded corners (described by a BorderRadius). The edges of the rectangle will match the edges of the box into which the Border or BoxDecoration is painted.

See also:

 *  RoundedRectangleBorder, the equivalent ShapeBorder.

`const BoxShape(0)`

values → const List<BoxShape>

A constant List of the values in this enum, in order of their declaration.

`const List<BoxShape>`

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/painting/box_border.dart#L22