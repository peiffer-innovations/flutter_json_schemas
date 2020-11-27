[*description*][description]

# FloatingLabelBehavior enum #

Defines the behavior of the floating label.

## Constants ##

always → const FloatingLabelBehavior

The label will always float above the content.

`const FloatingLabelBehavior(2)`

auto → const FloatingLabelBehavior

The label will float when the input is focused, or has content.

`const FloatingLabelBehavior(1)`

never → const FloatingLabelBehavior

The label will always be positioned within the content, or hidden.

`const FloatingLabelBehavior(0)`

values → const List<FloatingLabelBehavior>

A constant List of the values in this enum, in order of their declaration.

`const List<FloatingLabelBehavior>`

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/input_decorator.dart#L472