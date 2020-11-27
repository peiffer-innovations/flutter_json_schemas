[*description*][description]

# Overflow enum Null safety #

Whether overflowing children should be clipped, or their overflow be visible.

## Constants ##

clip → const Overflow

Overflowing children will be clipped to the bounds of their parent.

`const Overflow(1)`

values → const List<Overflow>

A constant List of the values in this enum, in order of their declaration.

`const List<Overflow>`

visible → const Overflow

Overflowing children will be visible.

The visible overflow area will not accept hit testing.

`const Overflow(0)`

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/rendering/stack.dart#L275