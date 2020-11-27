# Radius class Null safety #

A radius for either circular or elliptical shapes.

## Constructors ##

Radius.circular(double radius)

Constructs a circular radius. x and y will have the same radius value.

const

Radius.elliptical(double x, double y)

Constructs an elliptical radius with the given radii.

const

## Properties ##

hashCode → int

The hash code for this object. \[...\]

read-only, override

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

x → double

The radius value on the horizontal axis.

final

y → double

The radius value on the vertical axis.

final

## Methods ##

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

toString() → String

Returns a string representation of this object.

override

## Operators ##

operator %(double operand) → Radius

Modulo (remainder) operator. \[...\]

operator \*(double operand) → Radius

Multiplication operator. \[...\]

operator +(Radius other) → Radius

Binary addition operator. \[...\]

operator -(Radius other) → Radius

Binary subtraction operator. \[...\]

operator /(double operand) → Radius

Division operator. \[...\]

operator ==(Object other) → bool

The equality operator. \[...\]

override

operator unary-() → Radius

Unary negation operator. \[...\]

operator ~/(double operand) → Radius

Integer (truncating) division operator. \[...\]

## Static Methods ##

lerp(Radius? a, Radius? b, double t) → Radius?

Linearly interpolate between two radii. \[...\]

## Constants ##

zero → const Radius

A radius with x and y values set to zero. \[...\]

`const Radius.circular(0.0)`