[*description*][description]

# ButtonTextTheme enum #

Used with ButtonTheme and ButtonThemeData to define a button's base colors, and the defaults for the button's minimum size, internal padding, and shape.

See also:

 *  RaisedButton, FlatButton, OutlineButton, which are configured based on the ambient ButtonTheme.

## Constants ##

accent → const ButtonTextTheme

Button text is ThemeData.accentColor.

`const ButtonTextTheme(1)`

normal → const ButtonTextTheme

Button text is black or white depending on ThemeData.brightness.

`const ButtonTextTheme(0)`

primary → const ButtonTextTheme

Button text is based on ThemeData.primaryColor.

`const ButtonTextTheme(2)`

values → const List<ButtonTextTheme>

A constant List of the values in this enum, in order of their declaration.

`const List<ButtonTextTheme>`

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/button_theme.dart#L29