[*description*][description]

# ButtonBarLayoutBehavior enum #

Used with ButtonTheme and ButtonThemeData to define how the button bar should size itself with either constraints or internal padding.

## Constants ##

constrained → const ButtonBarLayoutBehavior

Button bars will be constrained to a minimum height of 52.

This setting is require to create button bars which conform to the material specification.

`const ButtonBarLayoutBehavior(0)`

padded → const ButtonBarLayoutBehavior

Button bars will calculate their padding from the button theme padding.

`const ButtonBarLayoutBehavior(1)`

values → const List<ButtonBarLayoutBehavior>

A constant List of the values in this enum, in order of their declaration.

`const List<ButtonBarLayoutBehavior>`

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/button_theme.dart#L42