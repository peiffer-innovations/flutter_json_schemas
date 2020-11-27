[*description*][description]

# BorderRadius class Null safety #

An immutable set of radii for each corner of a rectangle.

Used by BoxDecoration when the shape is a BoxShape.rectangle.

The BorderRadius class specifies offsets in terms of visual corners, e.g. topLeft. These values are not affected by the TextDirection. To support both left-to-right and right-to-left layouts, consider using BorderRadiusDirectional, which is expressed in terms that are relative to a TextDirection (typically obtained from the ambient Directionality).

Inheritance

 *  Object
 *  BorderRadiusGeometry
 *  BorderRadius

## Constructors ##

BorderRadius.all(Radius radius)

Creates a border radius where all radii are `radius`.

const

BorderRadius.circular(double radius)

Creates a border radius where all radii are Radius.circular(radius).

BorderRadius.horizontal(\{Radius left: Radius.zero, Radius right: Radius.zero\})

Creates a horizontally symmetrical border radius where the left and right sides of the rectangle have the same radii.

const

BorderRadius.only(\{Radius topLeft: Radius.zero, Radius topRight: Radius.zero, Radius bottomLeft: Radius.zero, Radius bottomRight: Radius.zero\})

Creates a border radius with only the given non-zero values. The other corners will be right angles.

const

BorderRadius.vertical(\{Radius top: Radius.zero, Radius bottom: Radius.zero\})

Creates a vertically symmetric border radius where the top and bottom sides of the rectangle have the same radii.

const

## Properties ##

bottomLeft → Radius

The bottom-left Radius.

final

bottomRight → Radius

The bottom-right Radius.

final

hashCode → int

The hash code for this object. \[...\]

read-only, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

topLeft → Radius

The top-left Radius.

final

topRight → Radius

The top-right Radius.

final

## Methods ##

add(BorderRadiusGeometry other) → BorderRadiusGeometry

Returns the sum of two BorderRadiusGeometry objects. \[...\]

override

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

resolve(TextDirection? direction) → BorderRadius

Convert this instance into a BorderRadius, so that the radii are expressed for specific physical corners (top-left, top-right, etc) rather than in a direction-dependent manner. \[...\]

override

subtract(BorderRadiusGeometry other) → BorderRadiusGeometry

Returns the difference between two BorderRadiusGeometry objects. \[...\]

override

toRRect(Rect rect) → RRect

Creates an RRect from the current border radius and a Rect.

toString() → String

Returns a string representation of this object.

inherited

## Operators ##

operator %(double other) → BorderRadius

Computes the remainder of each corner by the given factor.

override

operator \*(double other) → BorderRadius

Scales each corner of the BorderRadius by the given factor.

override

operator +(BorderRadius other) → BorderRadius

Returns the sum of two BorderRadius objects.

operator -(BorderRadius other) → BorderRadius

Returns the difference between two BorderRadius objects.

operator /(double other) → BorderRadius

Divides each corner of the BorderRadius by the given factor.

override

operator ==(Object other) → bool

The equality operator. \[...\]

inherited

operator unary-() → BorderRadius

Returns the BorderRadius object with each corner negated. \[...\]

override

operator ~/(double other) → BorderRadius

Integer divides each corner of the BorderRadius by the given factor.

override

## Static Methods ##

lerp(BorderRadius? a, BorderRadius? b, double t) → BorderRadius?

Linearly interpolate between two BorderRadius objects. \[...\]

override

## Constants ##

zero → const BorderRadius

A border radius with all zero radii.

`BorderRadius.all(Radius.zero)`


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/painting/border_radius.dart#L283