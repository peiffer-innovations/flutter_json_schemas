[*description*][description]

# EdgeInsetsGeometry class Null safety #

Base class for EdgeInsets that allows for text-direction aware resolution.

A property or argument of this type accepts classes created either with new EdgeInsets.fromLTRB and its variants, or new EdgeInsetsDirectional.fromSTEB and its variants.

To convert an EdgeInsetsGeometry object of indeterminate type into a EdgeInsets object, call the resolve method.

See also:

 *  Padding, a widget that describes margins using EdgeInsetsGeometry.

Implementers

 *  EdgeInsets
 *  EdgeInsetsDirectional

Annotations

 *  @immutable

## Constructors ##

EdgeInsetsGeometry()

Abstract const constructor. This constructor enables subclasses to provide const constructors so that they can be used in const expressions.

const

## Properties ##

collapsedSize → Size

The size that this EdgeInsets would occupy with an empty interior.

read-only

flipped → EdgeInsetsGeometry

An EdgeInsetsGeometry with top and bottom, left and right, and start and end flipped.

read-only

hashCode → int

The hash code for this object. \[...\]

read-only, override

horizontal → double

The total offset in the horizontal direction.

read-only

isNonNegative → bool

Whether every dimension is non-negative.

read-only

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

vertical → double

The total offset in the vertical direction.

read-only

## Methods ##

add(EdgeInsetsGeometry other) → EdgeInsetsGeometry

Returns the sum of two EdgeInsetsGeometry objects. \[...\]

along(Axis axis) → double

The total offset in the given direction.

clamp(EdgeInsetsGeometry min, EdgeInsetsGeometry max) → EdgeInsetsGeometry

Returns the a new EdgeInsetsGeometry object with all values greater than or equal to `min`, and less than or equal to `max`.

deflateSize(Size size) → Size

Returns a new size that is smaller than the given size by the amount of inset in the horizontal and vertical directions. \[...\]

inflateSize(Size size) → Size

Returns a new size that is bigger than the given size by the amount of inset in the horizontal and vertical directions. \[...\]

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

resolve(TextDirection? direction) → EdgeInsets

Convert this instance into an EdgeInsets, which uses literal coordinates (i.e. the `left` coordinate being explicitly a distance from the left, and the `right` coordinate being explicitly a distance from the right). \[...\]

subtract(EdgeInsetsGeometry other) → EdgeInsetsGeometry

Returns the difference between two EdgeInsetsGeometry objects. \[...\]

toString() → String

Returns a string representation of this object.

override

## Operators ##

operator %(double other) → EdgeInsetsGeometry

Computes the remainder in each dimension by the given factor. \[...\]

operator \*(double other) → EdgeInsetsGeometry

Scales the EdgeInsetsGeometry object in each dimension by the given factor. \[...\]

operator /(double other) → EdgeInsetsGeometry

Divides the EdgeInsetsGeometry object in each dimension by the given factor. \[...\]

operator ==(Object other) → bool

The equality operator. \[...\]

override

operator unary-() → EdgeInsetsGeometry

Returns the EdgeInsetsGeometry object with each dimension negated. \[...\]

operator ~/(double other) → EdgeInsetsGeometry

Integer divides the EdgeInsetsGeometry object in each dimension by the given factor. \[...\]

## Static Methods ##

lerp(EdgeInsetsGeometry? a, EdgeInsetsGeometry? b, double t) → EdgeInsetsGeometry?

Linearly interpolate between two EdgeInsetsGeometry objects. \[...\]

## Constants ##

infinity → const EdgeInsetsGeometry

An EdgeInsetsGeometry with infinite offsets in each direction. \[...\]

`_MixedEdgeInsets.fromLRSETB(double.infinity, double.infinity, double.infinity, double.infinity, double.infinity, double.infinity)`


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/painting/edge_insets.dart#L26