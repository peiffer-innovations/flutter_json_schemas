[*description*][description]

# BoxShadow class Null safety #

A shadow cast by a box.

BoxShadow can cast non-rectangular shadows if the box is non-rectangular (e.g., has a border radius or a circular shape).

This class is similar to CSS box-shadow.

See also:

 *  Canvas.drawShadow, which is a more efficient way to draw shadows.
 *  PhysicalModel, a widget for showing shadows.
 *  kElevationToShadow, for some predefined shadows used in Material Design.
 *  Shadow, which is the parent class that lacks spreadRadius.

Inheritance

 *  Object
 *  Shadow
 *  BoxShadow

Annotations

 *  @immutable

## Constructors ##

BoxShadow(\{Color color: const Color(0xFF000000), Offset offset: Offset.zero, double blurRadius: 0.0, double spreadRadius: 0.0\})

Creates a box shadow. \[...\]

const

## Properties ##

blurRadius → double

The standard deviation of the Gaussian to convolve with the shadow's shape.

final, inherited

blurSigma → double

The blurRadius in sigmas instead of logical pixels. \[...\]

read-only, inherited

color → Color

Color that the shadow will be drawn with. \[...\]

final, inherited

hashCode → int

The hash code for this object. \[...\]

read-only, override

offset → Offset

The displacement of the shadow from the casting element. \[...\]

final, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

spreadRadius → double

The amount the box should be inflated prior to applying the blur.

final

## Methods ##

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

scale(double factor) → BoxShadow

Returns a new box shadow with its offset, blurRadius, and spreadRadius scaled by the given factor.

override

toPaint() → Paint

Create the Paint object that corresponds to this shadow description. \[...\]

override

toString() → String

Returns a string representation of this object.

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

override

## Static Methods ##

lerp(BoxShadow? a, BoxShadow? b, double t) → BoxShadow?

Linearly interpolate between two box shadows. \[...\]

override

lerpList(List<BoxShadow>? a, List<BoxShadow>? b, double t) → List<BoxShadow>?

Linearly interpolate between two lists of box shadows. \[...\]

override


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/painting/box_shadow.dart#L29