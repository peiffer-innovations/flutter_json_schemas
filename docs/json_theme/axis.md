[*description*][description]

# Axis enum Null safety #

The two cardinal directions in two dimensions.

The axis is always relative to the current coordinate space. This means, for example, that a horizontal axis might actually be diagonally from top right to bottom left, due to some local Transform applied to the scene.

See also:

 *  AxisDirection, which is a directional version of this enum (with values light left and right, rather than just horizontal).
 *  TextDirection, which disambiguates between left-to-right horizontal content and right-to-left horizontal content.

## Constants ##

horizontal → const Axis

Left and right.

See also:

 *  TextDirection, which disambiguates between left-to-right horizontal content and right-to-left horizontal content.

`const Axis(0)`

values → const List<Axis>

A constant List of the values in this enum, in order of their declaration.

`const List<Axis>`

vertical → const Axis

Up and down.

`const Axis(1)`

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/painting/basic_types.dart#L116