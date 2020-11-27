# Size class Null safety #

Holds a 2D floating-point size.

You can think of this as an Offset from the origin.

Inheritance

 *  Object
 *  OffsetBase
 *  Size

## Constructors ##

Size(double width, double height)

Creates a Size with the given `width` and `height`.

const

Size.copy(Size source)

Creates an instance of Size that has the same values as another.

Size.fromHeight(double height)

Creates a Size with the given `height` and an infinite width.

const

Size.fromRadius(double radius)

Creates a square Size whose width and height are twice the given dimension. \[...\]

const

Size.fromWidth(double width)

Creates a Size with the given `width` and an infinite height.

const

Size.square(double dimension)

Creates a square Size whose width and height are the given dimension. \[...\]

const

## Properties ##

aspectRatio → double

The aspect ratio of this size. \[...\]

read-only

flipped → Size

A Size with the width and height swapped.

read-only

hashCode → int

The hash code for this object. \[...\]

read-only, override

height → double

The vertical extent of this size.

read-only

isEmpty → bool

Whether this size encloses a non-zero area. \[...\]

read-only

isFinite → bool

Whether both components are finite (neither infinite nor NaN). \[...\]

read-only, inherited

isInfinite → bool

Returns true if either component is double.infinity, and false if both are finite (or negative infinity, or NaN). \[...\]

read-only, inherited

longestSide → double

The greater of the magnitudes of the width and the height.

read-only

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

shortestSide → double

The lesser of the magnitudes of the width and the height.

read-only

width → double

The horizontal extent of this size.

read-only

## Methods ##

bottomCenter(Offset origin) → Offset

The offset to the center of the bottom edge of the rectangle described by the given offset (which is interpreted as the top-left corner) and this size. \[...\]

bottomLeft(Offset origin) → Offset

The offset to the intersection of the bottom and left edges of the rectangle described by the given offset (which is interpreted as the top-left corner) and this size. \[...\]

bottomRight(Offset origin) → Offset

The offset to the intersection of the bottom and right edges of the rectangle described by the given offset (which is interpreted as the top-left corner) and this size. \[...\]

center(Offset origin) → Offset

The offset to the point halfway between the left and right and the top and bottom edges of the rectangle described by the given offset (which is interpreted as the top-left corner) and this size. \[...\]

centerLeft(Offset origin) → Offset

The offset to the center of the left edge of the rectangle described by the given offset (which is interpreted as the top-left corner) and this size. \[...\]

centerRight(Offset origin) → Offset

The offset to the center of the right edge of the rectangle described by the given offset (which is interpreted as the top-left corner) and this size. \[...\]

contains(Offset offset) → bool

Whether the point specified by the given offset (which is assumed to be relative to the top left of the size) lies between the left and right and the top and bottom edges of a rectangle of this size. \[...\]

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

topCenter(Offset origin) → Offset

The offset to the center of the top edge of the rectangle described by the given offset (which is interpreted as the top-left corner) and this size. \[...\]

topLeft(Offset origin) → Offset

The offset to the intersection of the top and left edges of the rectangle described by the given Offset (which is interpreted as the top-left corner) and this Size. \[...\]

topRight(Offset origin) → Offset

The offset to the intersection of the top and right edges of the rectangle described by the given offset (which is interpreted as the top-left corner) and this size. \[...\]

toString() → String

Returns a string representation of this object.

override

## Operators ##

operator %(double operand) → Size

Modulo (remainder) operator. \[...\]

operator \*(double operand) → Size

Multiplication operator. \[...\]

operator +(Offset other) → Size

Binary addition operator for adding an Offset to a Size. \[...\]

operator -(OffsetBase other) → OffsetBase

Binary subtraction operator for Size. \[...\]

operator /(double operand) → Size

Division operator. \[...\]

operator <(OffsetBase other) → bool

Less-than operator. Compares an Offset or Size to another Offset or Size, and returns true if both the horizontal and vertical values of the left-hand-side operand are smaller than the horizontal and vertical values of the right-hand-side operand respectively. Returns false otherwise. \[...\]

inherited

operator <=(OffsetBase other) → bool

Less-than-or-equal-to operator. Compares an Offset or Size to another Offset or Size, and returns true if both the horizontal and vertical values of the left-hand-side operand are smaller than or equal to the horizontal and vertical values of the right-hand-side operand respectively. Returns false otherwise. \[...\]

inherited

operator ==(Object other) → bool

Compares two Sizes for equality.

override

operator >(OffsetBase other) → bool

Greater-than operator. Compares an Offset or Size to another Offset or Size, and returns true if both the horizontal and vertical values of the left-hand-side operand are bigger than the horizontal and vertical values of the right-hand-side operand respectively. Returns false otherwise. \[...\]

inherited

operator >=(OffsetBase other) → bool

Greater-than-or-equal-to operator. Compares an Offset or Size to another Offset or Size, and returns true if both the horizontal and vertical values of the left-hand-side operand are bigger than or equal to the horizontal and vertical values of the right-hand-side operand respectively. Returns false otherwise. \[...\]

inherited

operator ~/(double operand) → Size

Integer (truncating) division operator. \[...\]

## Static Methods ##

lerp(Size? a, Size? b, double t) → Size?

Linearly interpolate between two sizes \[...\]

## Constants ##

infinite → const Size

A size whose width and height are infinite. \[...\]

`Size(double.infinity, double.infinity)`

zero → const Size

An empty size, one with a zero width and a zero height.

`Size(0.0, 0.0)`