[*description*][description]

# NotchedShape class Null safety #

A shape with a notch in its outline.

Typically used as the outline of a 'host' widget to make a notch that accommodates a 'guest' widget. e.g the BottomAppBar may have a notch to accommodate the FloatingActionButton.

See also:

 *  ShapeBorder, which defines a shaped border without a dynamic notch.
 *  AutomaticNotchedShape, an adapter from ShapeBorder to NotchedShape.

Implementers

 *  AutomaticNotchedShape
 *  CircularNotchedRectangle

## Constructors ##

NotchedShape()

Abstract const constructor. This constructor enables subclasses to provide const constructors so that they can be used in const expressions.

const

## Properties ##

hashCode → int

The hash code for this object. \[...\]

read-only, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

getOuterPath(Rect host, Rect? guest) → Path

Creates a Path that describes the outline of the shape. \[...\]

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

toString() → String

Returns a string representation of this object.

inherited

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/painting/notched_shapes.dart#L21