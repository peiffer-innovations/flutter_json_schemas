# Rect class Null safety #

An immutable, 2D, axis-aligned, floating-point rectangle whose coordinates are relative to a given origin.

A Rect can be created with one its constructors or from an Offset and a Size using the `&` operator:

    Rect myRect = const Offset(1.0, 2.0) & const Size(3.0, 4.0);

## Constructors ##

Rect.fromCenter(\{required Offset center, required double width, required double height\})

Constructs a rectangle from its center point, width, and height. \[...\]

Rect.fromCircle(\{required Offset center, required double radius\})

Construct a rectangle that bounds the given circle. \[...\]

Rect.fromLTRB(double left, double top, double right, double bottom)

Construct a rectangle from its left, top, right, and bottom edges.

const

Rect.fromLTWH(double left, double top, double width, double height)

Construct a rectangle from its left and top edges, its width, and its height. \[...\]

const

Rect.fromPoints(Offset a, Offset b)

Construct the smallest rectangle that encloses the given offsets, treating them as vectors from the origin.

## Properties ##

bottom → double

The offset of the bottom edge of this rectangle from the y axis.

final

bottomCenter → Offset

The offset to the center of the bottom edge of this rectangle. \[...\]

read-only

bottomLeft → Offset

The offset to the intersection of the bottom and left edges of this rectangle. \[...\]

read-only

bottomRight → Offset

The offset to the intersection of the bottom and right edges of this rectangle. \[...\]

read-only

center → Offset

The offset to the point halfway between the left and right and the top and bottom edges of this rectangle. \[...\]

read-only

centerLeft → Offset

The offset to the center of the left edge of this rectangle. \[...\]

read-only

centerRight → Offset

The offset to the center of the right edge of this rectangle. \[...\]

read-only

hashCode → int

The hash code for this object. \[...\]

read-only, override

hasNaN → bool

Whether any of the dimensions are `NaN`.

read-only

height → double

The distance between the top and bottom edges of this rectangle.

read-only

isEmpty → bool

Whether this rectangle encloses a non-zero area. Negative areas are considered empty.

read-only

isFinite → bool

Whether all coordinates of this rectangle are finite.

read-only

isInfinite → bool

Whether any of the coordinates of this rectangle are equal to positive infinity.

read-only

left → double

The offset of the left edge of this rectangle from the x axis.

final

longestSide → double

The greater of the magnitudes of the width and the height of this rectangle.

read-only

right → double

The offset of the right edge of this rectangle from the x axis.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

shortestSide → double

The lesser of the magnitudes of the width and the height of this rectangle.

read-only

size → Size

The distance between the upper-left corner and the lower-right corner of this rectangle.

read-only

top → double

The offset of the top edge of this rectangle from the y axis.

final

topCenter → Offset

The offset to the center of the top edge of this rectangle. \[...\]

read-only

topLeft → Offset

The offset to the intersection of the top and left edges of this rectangle. \[...\]

read-only

topRight → Offset

The offset to the intersection of the top and right edges of this rectangle. \[...\]

read-only

width → double

The distance between the left and right edges of this rectangle.

read-only

## Methods ##

contains(Offset offset) → bool

Whether the point specified by the given offset (which is assumed to be relative to the origin) lies between the left and right and the top and bottom edges of this rectangle. \[...\]

deflate(double delta) → Rect

Returns a new rectangle with edges moved inwards by the given delta.

expandToInclude(Rect other) → Rect

Returns a new rectangle which is the bounding box containing this rectangle and the given rectangle.

inflate(double delta) → Rect

Returns a new rectangle with edges moved outwards by the given delta.

intersect(Rect other) → Rect

Returns a new rectangle that is the intersection of the given rectangle and this rectangle. The two rectangles must overlap for this to be meaningful. If the two rectangles do not overlap, then the resulting Rect will have a negative width or height.

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

overlaps(Rect other) → bool

Whether `other` has a nonzero area of overlap with this rectangle.

shift(Offset offset) → Rect

Returns a new rectangle translated by the given offset. \[...\]

toString() → String

Returns a string representation of this object.

override

translate(double translateX, double translateY) → Rect

Returns a new rectangle with translateX added to the x components and translateY added to the y components. \[...\]

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

override

## Static Methods ##

lerp(Rect? a, Rect? b, double t) → Rect?

Linearly interpolate between two rectangles. \[...\]

## Constants ##

largest → const Rect

A rectangle that covers the entire coordinate space. \[...\]

`const Rect.fromLTRB(-_giantScalar, -_giantScalar, _giantScalar, _giantScalar)`

zero → const Rect

A rectangle with left, top, right, and bottom edges all at zero.

`const Rect.fromLTRB(0.0, 0.0, 0.0, 0.0)`