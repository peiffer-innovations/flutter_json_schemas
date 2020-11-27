# Shadow class Null safety #

A single shadow.

Multiple shadows are stacked together in a TextStyle.

Implementers

 *  BoxShadow

## Constructors ##

Shadow(\{Color color: const Color(\_kColorDefault), Offset offset: Offset.zero, double blurRadius: 0.0\})

Construct a shadow. \[...\]

const

## Properties ##

blurRadius → double

The standard deviation of the Gaussian to convolve with the shadow's shape.

final

blurSigma → double

The blurRadius in sigmas instead of logical pixels. \[...\]

read-only

color → Color

Color that the shadow will be drawn with. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

offset → Offset

The displacement of the shadow from the casting element. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

scale(double factor) → Shadow

Returns a new shadow with its offset and blurRadius scaled by the given factor.

toPaint() → Paint

Create the Paint object that corresponds to this shadow description. \[...\]

toString() → String

Returns a string representation of this object.

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

override

## Static Methods ##

convertRadiusToSigma(double radius) → double

Converts a blur radius in pixels to sigmas. \[...\]

lerp(Shadow? a, Shadow? b, double t) → Shadow?

Linearly interpolate between two shadows. \[...\]

lerpList(List<Shadow>? a, List<Shadow>? b, double t) → List<Shadow>?

Linearly interpolate between two lists of shadows. \[...\]