[*description*][description]

# ShapeBorder class Null safety #

Base class for shape outlines.

This class handles how to add multiple borders together. Subclasses define various shapes, like circles (CircleBorder), rounded rectangles (RoundedRectangleBorder), continuous rectangles (ContinuousRectangleBorder), or beveled rectangles (BeveledRectangleBorder).

See also:

 *  ShapeDecoration, which can be used with DecoratedBox to show a shape.
 *  Material (and many other widgets in the Material library), which takes a ShapeBorder to define its shape.
 *  NotchedShape, which describes a shape with a hole in it.

Implementers

 *  BoxBorder
 *  InputBorder
 *  OutlinedBorder

Annotations

 *  @immutable

## Constructors ##

ShapeBorder()

Abstract const constructor. This constructor enables subclasses to provide const constructors so that they can be used in const expressions.

const

## Properties ##

dimensions → EdgeInsetsGeometry

The widths of the sides of this border represented as an EdgeInsets. \[...\]

read-only

hashCode → int

The hash code for this object. \[...\]

read-only, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

add(ShapeBorder other, \{bool reversed: false\}) → ShapeBorder?

Attempts to create a new object that represents the amalgamation of `this` border and the `other` border. \[...\]

@protected

getInnerPath(Rect rect, \{TextDirection? textDirection\}) → Path

Create a Path that describes the inner edge of the border. \[...\]

getOuterPath(Rect rect, \{TextDirection? textDirection\}) → Path

Create a Path that describes the outer edge of the border. \[...\]

lerpFrom(ShapeBorder? a, double t) → ShapeBorder?

Linearly interpolates from another ShapeBorder (possibly of another class) to `this`. \[...\]

@protected

lerpTo(ShapeBorder? b, double t) → ShapeBorder?

Linearly interpolates from `this` to another ShapeBorder (possibly of another class). \[...\]

@protected

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

paint(Canvas canvas, Rect rect, \{TextDirection? textDirection\}) → void

Paints the border within the given Rect on the given Canvas. \[...\]

scale(double t) → ShapeBorder

Creates a copy of this border, scaled by the factor `t`. \[...\]

toString() → String

Returns a string representation of this object.

override

## Operators ##

operator +(ShapeBorder other) → ShapeBorder

Creates a new border consisting of the two borders on either side of the operator. \[...\]

operator ==(Object other) → bool

The equality operator. \[...\]

inherited

## Static Methods ##

lerp(ShapeBorder? a, ShapeBorder? b, double t) → ShapeBorder?

Linearly interpolates between two ShapeBorders. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/painting/borders.dart#L288