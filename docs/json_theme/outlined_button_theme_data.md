[*description*][description]

# OutlinedButtonThemeData class #

A ButtonStyle that overrides the default appearance of OutlinedButtons when it's used with OutlinedButtonTheme or with the overall Theme's ThemeData.outlinedButtonTheme.

The style's properties override OutlinedButton's default style, i.e. the ButtonStyle returned by OutlinedButton.defaultStyleOf. Only the style's non-null property values or resolved non-null MaterialStateProperty values are used.

See also:

 *  OutlinedButtonTheme, the theme which is configured with this class.
 *  OutlinedButton.defaultStyleOf, which returns the default ButtonStyle for outlined buttons.
 *  OutlinedButton.styleFrom, which converts simple values into a ButtonStyle that's consistent with OutlinedButton's defaults.
 *  MaterialStateProperty.resolve, "resolve" a material state property to a simple value based on a set of MaterialStates.
 *  ThemeData.outlinedButtonTheme, which can be used to override the default ButtonStyle for OutlinedButtons below the overall Theme.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

OutlinedButtonThemeData(\{ButtonStyle style\})

Creates a OutlinedButtonThemeData. \[...\]

const

## Properties ##

hashCode → int

The hash code for this object. \[...\]

read-only, override

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

style → ButtonStyle

Overrides for OutlinedButton's default style. \[...\]

final

## Methods ##

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

override

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

toDiagnosticsNode(\{String name, DiagnosticsTreeStyle style\}) → DiagnosticsNode

Returns a debug representation of the object that is used by debugging tools and by DiagnosticsNode.toStringDeep. \[...\]

inherited

toString(\{DiagnosticLevel minLevel: DiagnosticLevel.info\}) → String

Returns a string representation of this object.

inherited

toStringShort() → String

A brief description of this object, usually just the runtimeType and the hashCode. \[...\]

inherited

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

override

## Static Methods ##

lerp(OutlinedButtonThemeData a, OutlinedButtonThemeData b, double t) → OutlinedButtonThemeData

Linearly interpolate between two outlined button themes.


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/outlined_button_theme.dart#L34