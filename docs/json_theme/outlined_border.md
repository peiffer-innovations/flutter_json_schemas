[*description*][description]

# OutlinedBorder class Null safety #

A ShapeBorder that draws an outline with the width and color specified by side.

Inheritance

 *  Object
 *  ShapeBorder
 *  OutlinedBorder

Implementers

 *  BeveledRectangleBorder
 *  CircleBorder
 *  ContinuousRectangleBorder
 *  RoundedRectangleBorder
 *  StadiumBorder

Annotations

 *  @immutable

## Constructors ##

OutlinedBorder(\{BorderSide side: BorderSide.none\})

Abstract const constructor. This constructor enables subclasses to provide const constructors so that they can be used in const expressions. \[...\]

const

## Properties ##

dimensions → EdgeInsetsGeometry

The widths of the sides of this border represented as an EdgeInsets. \[...\]

read-only, inherited

hashCode → int

The hash code for this object. \[...\]

read-only, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

side → BorderSide

The border outline's color and weight. \[...\]

final

## Methods ##

add(ShapeBorder other, \{bool reversed: false\}) → ShapeBorder?

Attempts to create a new object that represents the amalgamation of `this` border and the `other` border. \[...\]

@protected, inherited

copyWith(\{BorderSide? side\}) → OutlinedBorder

Returns a copy of this OutlinedBorder that draws its outline with the specified `side`, if `side` is non-null.

getInnerPath(Rect rect, \{TextDirection? textDirection\}) → Path

Create a Path that describes the inner edge of the border. \[...\]

inherited

getOuterPath(Rect rect, \{TextDirection? textDirection\}) → Path

Create a Path that describes the outer edge of the border. \[...\]

inherited

lerpFrom(ShapeBorder? a, double t) → ShapeBorder?

Linearly interpolates from another ShapeBorder (possibly of another class) to `this`. \[...\]

@protected, inherited

lerpTo(ShapeBorder? b, double t) → ShapeBorder?

Linearly interpolates from `this` to another ShapeBorder (possibly of another class). \[...\]

@protected, inherited

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

paint(Canvas canvas, Rect rect, \{TextDirection? textDirection\}) → void

Paints the border within the given Rect on the given Canvas. \[...\]

inherited

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/painting/borders.dart#L498