# Offset class Null safety #

An immutable 2D floating-point offset.

Generally speaking, Offsets can be interpreted in two ways:

1.  As representing a point in Cartesian space a specified distance from a separately-maintained origin. For example, the top-left position of children in the RenderBox protocol is typically represented as an Offset from the top left of the parent box.
2.  As a vector that can be applied to coordinates. For example, when painting a RenderObject, the parent is passed an Offset from the screen's origin which it can add to the offsets of its children to find the Offset from the screen's origin to each of the children.

Because a particular Offset can be interpreted as one sense at one time then as the other sense at a later time, the same class is used for both senses.

See also:

 *  Size, which represents a vector describing the size of a rectangle.

Inheritance

 *  Object
 *  OffsetBase
 *  Offset

## Constructors ##

Offset(double dx, double dy)

Creates an offset. The first argument sets `dx`, the horizontal component, and the second sets `dy`, the vertical component.

const

Offset.fromDirection(double direction, \[double distance = 1.0\])

Creates an offset from its `direction` and `distance`. \[...\]

factory

## Properties ##

direction → double

The angle of this offset as radians clockwise from the positive x-axis, in the range -pi to pi, assuming positive values of the x-axis go to the left and positive values of the y-axis go down. \[...\]

read-only

distance → double

The magnitude of the offset. \[...\]

read-only

distanceSquared → double

The square of the magnitude of the offset. \[...\]

read-only

dx → double

The x component of the offset. \[...\]

read-only

dy → double

The y component of the offset. \[...\]

read-only

hashCode → int

The hash code for this object. \[...\]

read-only, override

isFinite → bool

Whether both components are finite (neither infinite nor NaN). \[...\]

read-only, inherited

isInfinite → bool

Returns true if either component is double.infinity, and false if both are finite (or negative infinity, or NaN). \[...\]

read-only, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

scale(double scaleX, double scaleY) → Offset

Returns a new offset with the x component scaled by `scaleX` and the y component scaled by `scaleY`. \[...\]

toString() → String

Returns a string representation of this object.

override

translate(double translateX, double translateY) → Offset

Returns a new offset with translateX added to the x component and translateY added to the y component. \[...\]

## Operators ##

operator %(double operand) → Offset

Modulo (remainder) operator. \[...\]

operator &(Size other) → Rect

Rectangle constructor operator. \[...\]

operator \*(double operand) → Offset

Multiplication operator. \[...\]

operator +(Offset other) → Offset

Binary addition operator. \[...\]

operator -(Offset other) → Offset

Binary subtraction operator. \[...\]

operator /(double operand) → Offset

Division operator. \[...\]

operator <(OffsetBase other) → bool

Less-than operator. Compares an Offset or Size to another Offset or Size, and returns true if both the horizontal and vertical values of the left-hand-side operand are smaller than the horizontal and vertical values of the right-hand-side operand respectively. Returns false otherwise. \[...\]

inherited

operator <=(OffsetBase other) → bool

Less-than-or-equal-to operator. Compares an Offset or Size to another Offset or Size, and returns true if both the horizontal and vertical values of the left-hand-side operand are smaller than or equal to the horizontal and vertical values of the right-hand-side operand respectively. Returns false otherwise. \[...\]

inherited

operator ==(Object other) → bool

Compares two Offsets for equality.

override

operator >(OffsetBase other) → bool

Greater-than operator. Compares an Offset or Size to another Offset or Size, and returns true if both the horizontal and vertical values of the left-hand-side operand are bigger than the horizontal and vertical values of the right-hand-side operand respectively. Returns false otherwise. \[...\]

inherited

operator >=(OffsetBase other) → bool

Greater-than-or-equal-to operator. Compares an Offset or Size to another Offset or Size, and returns true if both the horizontal and vertical values of the left-hand-side operand are bigger than or equal to the horizontal and vertical values of the right-hand-side operand respectively. Returns false otherwise. \[...\]

inherited

operator unary-() → Offset

Unary negation operator. \[...\]

operator ~/(double operand) → Offset

Integer (truncating) division operator. \[...\]

## Static Methods ##

lerp(Offset? a, Offset? b, double t) → Offset?

Linearly interpolate between two offsets. \[...\]

## Constants ##

infinite → const Offset

An offset with infinite x and y components. \[...\]

`const Offset(double.infinity, double.infinity)`

zero → const Offset

An offset with zero magnitude. \[...\]

`const Offset(0.0, 0.0)`