[*description*][description]

# AutovalidateMode enum #

Used to configure the auto validation of FormField and Form widgets.

## Constants ##

always → const AutovalidateMode

Used to auto-validate Form and FormField even without user interaction.

`const AutovalidateMode(1)`

disabled → const AutovalidateMode

No auto validation will occur.

`const AutovalidateMode(0)`

onUserInteraction → const AutovalidateMode

Used to auto-validate Form and FormField only after each user interaction.

`const AutovalidateMode(2)`

values → const List<AutovalidateMode>

A constant List of the values in this enum, in order of their declaration.

`const List<AutovalidateMode>`

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/form.dart#L533