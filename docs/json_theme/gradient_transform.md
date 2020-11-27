[*description*][description]

# GradientTransform class Null safety #

Base class for transforming gradient shaders without applying the same transform to the entire canvas.

For example, a SweepGradient normally starts its gradation at 3 o'clock and draws clockwise. To have the sweep appear to start at 6 o'clock, supply a GradientRotation of `pi/4` radians (i.e. 45 degrees).

Implementers

 *  GradientRotation

Annotations

 *  @immutable

## Constructors ##

GradientTransform()

A const constructor so that subclasses may be const.

const

## Properties ##

hashCode → int

The hash code for this object. \[...\]

read-only, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

toString() → String

Returns a string representation of this object.

inherited

transform(Rect bounds, \{TextDirection? textDirection\}) → Matrix4?

When a Gradient creates its Shader, it will call this method to determine what transform to apply to the shader for the given Rect and TextDirection. \[...\]

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/painting/gradient.dart#L70