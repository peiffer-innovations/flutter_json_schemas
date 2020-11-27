[*description*][description]

# Gradient class Null safety #

A 2D gradient.

This is an interface that allows LinearGradient, RadialGradient, and SweepGradient classes to be used interchangeably in BoxDecorations.

See also:

 *  Gradient, the class in the dart:ui library.

Implementers

 *  LinearGradient
 *  RadialGradient
 *  SweepGradient

Annotations

 *  @immutable

## Constructors ##

Gradient(\{required List<Color> colors, List<double>? stops, GradientTransform? transform\})

Initialize the gradient's colors and stops. \[...\]

const

## Properties ##

colors → List<Color>

The colors the gradient should obtain at each of the stops. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

read-only, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

stops → List<double>?

A list of values from 0.0 to 1.0 that denote fractions along the gradient. \[...\]

final

transform → GradientTransform?

The transform, if any, to apply to the gradient. \[...\]

final

## Methods ##

createShader(Rect rect, \{TextDirection? textDirection\}) → Shader

Creates a Shader for this gradient to fill the given rect. \[...\]

@factory

lerpFrom(Gradient? a, double t) → Gradient?

Linearly interpolates from another Gradient to `this`. \[...\]

@protected

lerpTo(Gradient? b, double t) → Gradient?

Linearly interpolates from `this` to another Gradient. \[...\]

@protected

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

scale(double factor) → Gradient

Returns a new gradient with its properties scaled by the given factor. \[...\]

toString() → String

Returns a string representation of this object.

inherited

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

inherited

## Static Methods ##

lerp(Gradient? a, Gradient? b, double t) → Gradient?

Linearly interpolates between two Gradients. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/painting/gradient.dart#L132