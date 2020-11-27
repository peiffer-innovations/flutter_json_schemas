[*description*][description]

# BoxBorder class Null safety #

Base class for box borders that can paint as rectangles, circles, or rounded rectangles.

This class is extended by Border and BorderDirectional to provide concrete versions of four-sided borders using different conventions for specifying the sides.

The only API difference that this class introduces over ShapeBorder is that its paint method takes additional arguments.

See also:

 *  BorderSide, which is used to describe each side of the box.
 *  RoundedRectangleBorder, another way of describing a box's border.
 *  CircleBorder, another way of describing a circle border.
 *  BoxDecoration, which uses a BoxBorder to describe its borders.

Inheritance

 *  Object
 *  ShapeBorder
 *  BoxBorder

Implementers

 *  Border
 *  BorderDirectional

## Constructors ##

BoxBorder()

Abstract const constructor. This constructor enables subclasses to provide const constructors so that they can be used in const expressions.

const

## Properties ##

bottom → BorderSide

The bottom side of this border.

read-only

dimensions → EdgeInsetsGeometry

The widths of the sides of this border represented as an EdgeInsets. \[...\]

read-only, inherited

hashCode → int

The hash code for this object. \[...\]

read-only, inherited

isUniform → bool

Whether all four sides of the border are identical. Uniform borders are typically more efficient to paint. \[...\]

read-only

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

top → BorderSide

The top side of this border. \[...\]

read-only

## Methods ##

add(ShapeBorder other, \{bool reversed: false\}) → BoxBorder?

Attempts to create a new object that represents the amalgamation of `this` border and the `other` border. \[...\]

override

getInnerPath(Rect rect, \{TextDirection? textDirection\}) → Path

Create a Path that describes the inner edge of the border. \[...\]

override

getOuterPath(Rect rect, \{TextDirection? textDirection\}) → Path

Create a Path that describes the outer edge of the border. \[...\]

override

lerpFrom(ShapeBorder? a, double t) → ShapeBorder?

Linearly interpolates from another ShapeBorder (possibly of another class) to `this`. \[...\]

@protected, inherited

lerpTo(ShapeBorder? b, double t) → ShapeBorder?

Linearly interpolates from `this` to another ShapeBorder (possibly of another class). \[...\]

@protected, inherited

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

paint(Canvas canvas, Rect rect, \{TextDirection? textDirection, BoxShape shape: BoxShape.rectangle, BorderRadius? borderRadius\}) → void

Paints the border within the given Rect on the given Canvas. \[...\]

override

scale(double t) → ShapeBorder

Creates a copy of this border, scaled by the factor `t`. \[...\]

inherited

toString() → String

Returns a string representation of this object.

inherited

## Operators ##

operator +(ShapeBorder other) → ShapeBorder

Creates a new border consisting of the two borders on either side of the operator. \[...\]

inherited

operator ==(Object other) → bool

The equality operator. \[...\]

inherited

## Static Methods ##

lerp(BoxBorder? a, BoxBorder? b, double t) → BoxBorder?

Linearly interpolate between two borders. \[...\]

override


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/painting/box_border.dart#L61