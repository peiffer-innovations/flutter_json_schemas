[*description*][description]

# InputBorder class #

Defines the appearance of an InputDecorator's border.

An input decorator's border is specified by InputDecoration.border.

The border is drawn relative to the input decorator's "container" which is the optionally filled area above the decorator's helper, error, and counter.

Input border's are decorated with a line whose weight and color are defined by borderSide. The input decorator's renderer animates the input border's appearance in response to state changes, like gaining or losing the focus, by creating new copies of its input border with copyWith.

See also:

 *  UnderlineInputBorder, the default InputDecorator border which draws a horizontal line at the bottom of the input decorator's container.
 *  OutlineInputBorder, an InputDecorator border which draws a rounded rectangle around the input decorator's container.
 *  InputDecoration, which is used to configure an InputDecorator.

Inheritance

 *  Object
 *  ShapeBorder
 *  InputBorder

Implementers

 *  OutlineInputBorder
 *  UnderlineInputBorder

## Constructors ##

InputBorder(\{BorderSide borderSide: BorderSide.none\})

Creates a border for an InputDecorator. \[...\]

const

## Properties ##

borderSide → BorderSide

Defines the border line's color and weight. \[...\]

final

dimensions → EdgeInsetsGeometry

The widths of the sides of this border represented as an EdgeInsets. \[...\]

read-only, inherited

hashCode → int

The hash code for this object. \[...\]

read-only, inherited

isOutline → bool

True if this border will enclose the InputDecorator's container. \[...\]

read-only

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

add(ShapeBorder other, \{bool reversed: false\}) → ShapeBorder

Attempts to create a new object that represents the amalgamation of `this` border and the `other` border. \[...\]

@protected, inherited

copyWith(\{BorderSide borderSide\}) → InputBorder

Creates a copy of this input border with the specified `borderSide`.

getInnerPath(Rect rect, \{TextDirection textDirection\}) → Path

Create a Path that describes the inner edge of the border. \[...\]

inherited

getOuterPath(Rect rect, \{TextDirection textDirection\}) → Path

Create a Path that describes the outer edge of the border. \[...\]

inherited

lerpFrom(ShapeBorder a, double t) → ShapeBorder

Linearly interpolates from another ShapeBorder (possibly of another class) to `this`. \[...\]

@protected, inherited

lerpTo(ShapeBorder b, double t) → ShapeBorder

Linearly interpolates from `this` to another ShapeBorder (possibly of another class). \[...\]

@protected, inherited

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

paint(Canvas canvas, Rect rect, \{double gapStart, double gapExtent: 0.0, double gapPercentage: 0.0, TextDirection textDirection\}) → void

Paint this input border on `canvas`. \[...\]

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

## Constants ##

none → const InputBorder

No input border. \[...\]

`_NoInputBorder()`


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/input_border.dart#L32