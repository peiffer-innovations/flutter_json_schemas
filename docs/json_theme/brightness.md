# Brightness enum Null safety #

Describes the contrast of a theme or color palette.

## Constants ##

dark → const Brightness

The color is dark and will require a light text color to achieve readable contrast.

For example, the color might be dark grey, requiring white text.

`const Brightness(0)`

light → const Brightness

The color is light and will require a dark text color to achieve readable contrast.

For example, the color might be bright white, requiring black text.

`const Brightness(1)`

values → const List<Brightness>

A constant List of the values in this enum, in order of their declaration.

`const List<Brightness>`

## Properties ##

hashCode → int

The hash code for this object. \[...\]

read-only, inherited

index → int

The integer index of this enum.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

toString() → String

Returns a string representation of this object.

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

inherited