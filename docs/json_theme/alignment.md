[*description*][description]

# Alignment class Null safety #

A point within a rectangle.

`Alignment(0.0, 0.0)` represents the center of the rectangle. The distance from -1.0 to +1.0 is the distance from one side of the rectangle to the other side of the rectangle. Therefore, 2.0 units horizontally (or vertically) is equivalent to the width (or height) of the rectangle.

`Alignment(-1.0, -1.0)` represents the top left of the rectangle.

`Alignment(1.0, 1.0)` represents the bottom right of the rectangle.

`Alignment(0.0, 3.0)` represents a point that is horizontally centered with respect to the rectangle and vertically below the bottom of the rectangle by the height of the rectangle.

`Alignment(0.0, -0.5)` represents a point that is horizontally centered with respect to the rectangle and vertically half way between the top edge and the center.

`Alignment(x, y)` in a rectangle with height h and width w describes the point (x \* w/2 + w/2, y \* h/2 + h/2) in the coordinate system of the rectangle.

Alignment uses visual coordinates, which means increasing x moves the point from left to right. To support layouts with a right-to-left TextDirection, consider using AlignmentDirectional, in which the direction the point moves when increasing the horizontal value depends on the TextDirection.

A variety of widgets use Alignment in their configuration, most notably:

 *  Align positions a child according to an Alignment.

See also:

 *  AlignmentDirectional, which has a horizontal coordinate orientation that depends on the TextDirection.
 *  AlignmentGeometry, which is an abstract type that is agnostic as to whether the horizontal direction depends on the TextDirection.

Inheritance

 *  Object
 *  AlignmentGeometry
 *  Alignment

Implementers

 *  FractionalOffset

## Constructors ##

Alignment(double x, double y)

Creates an alignment. \[...\]

const

## Properties ##

hashCode → int

The hash code for this object. \[...\]

read-only, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

x → double

The distance fraction in the horizontal direction. \[...\]

final

y → double

The distance fraction in the vertical direction. \[...\]

final

## Methods ##

add(AlignmentGeometry other) → AlignmentGeometry

Returns the sum of two AlignmentGeometry objects. \[...\]

override

alongOffset(Offset other) → Offset

Returns the offset that is this fraction in the direction of the given offset.

alongSize(Size other) → Offset

Returns the offset that is this fraction within the given size.

inscribe(Size size, Rect rect) → Rect

Returns a rect of the given size, aligned within given rect as specified by this alignment. \[...\]

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

resolve(TextDirection? direction) → Alignment

Convert this instance into an Alignment, which uses literal coordinates (the `x` coordinate being explicitly a distance from the left). \[...\]

override

toString() → String

Returns a string representation of this object.

override

withinRect(Rect rect) → Offset

Returns the point that is this fraction within the given rect.

## Operators ##

operator %(double other) → Alignment

Computes the remainder in each dimension by the given factor.

override

operator \*(double other) → Alignment

Scales the Alignment in each dimension by the given factor.

override

operator +(Alignment other) → Alignment

Returns the sum of two Alignments.

operator -(Alignment other) → Alignment

Returns the difference between two Alignments.

operator /(double other) → Alignment

Divides the Alignment in each dimension by the given factor.

override

operator ==(Object other) → bool

The equality operator. \[...\]

inherited

operator unary-() → Alignment

Returns the negation of the given Alignment.

override

operator ~/(double other) → Alignment

Integer divides the Alignment in each dimension by the given factor.

override

## Static Methods ##

lerp(Alignment? a, Alignment? b, double t) → Alignment?

Linearly interpolate between two Alignments. \[...\]

override

## Constants ##

bottomCenter → const Alignment

The center point along the bottom edge.

`Alignment(0.0, 1.0)`

bottomLeft → const Alignment

The bottom left corner.

`Alignment(-1.0, 1.0)`

bottomRight → const Alignment

The bottom right corner.

`Alignment(1.0, 1.0)`

center → const Alignment

The center point, both horizontally and vertically.

`Alignment(0.0, 0.0)`

centerLeft → const Alignment

The center point along the left edge.

`Alignment(-1.0, 0.0)`

centerRight → const Alignment

The center point along the right edge.

`Alignment(1.0, 0.0)`

topCenter → const Alignment

The center point along the top edge.

`Alignment(0.0, -1.0)`

topLeft → const Alignment

The top left corner.

`Alignment(-1.0, -1.0)`

topRight → const Alignment

The top right corner.

`Alignment(1.0, -1.0)`


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/painting/alignment.dart#L181