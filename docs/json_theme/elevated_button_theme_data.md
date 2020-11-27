[*description*][description]

# ElevatedButtonThemeData class #

A ButtonStyle that overrides the default appearance of ElevatedButtons when it's used with ElevatedButtonTheme or with the overall Theme's ThemeData.elevatedButtonTheme.

The style's properties override ElevatedButton's default style, i.e. the ButtonStyle returned by ElevatedButton.defaultStyleOf. Only the style's non-null property values or resolved non-null MaterialStateProperty values are used.

See also:

 *  ElevatedButtonTheme, the theme which is configured with this class.
 *  ElevatedButton.defaultStyleOf, which returns the default ButtonStyle for text buttons.
 *  ElevatedButton.styleFrom, which converts simple values into a ButtonStyle that's consistent with ElevatedButton's defaults.
 *  MaterialStateProperty.resolve, "resolve" a material state property to a simple value based on a set of MaterialStates.
 *  ThemeData.elevatedButtonTheme, which can be used to override the default ButtonStyle for ElevatedButtons below the overall Theme.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

ElevatedButtonThemeData(\{ButtonStyle style\})

Creates an ElevatedButtonThemeData. \[...\]

const

## Properties ##

hashCode → int

The hash code for this object. \[...\]

read-only, override

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

style → ButtonStyle

Overrides for ElevatedButton's default style. \[...\]

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

lerp(ElevatedButtonThemeData a, ElevatedButtonThemeData b, double t) → ElevatedButtonThemeData

Linearly interpolate between two elevated button themes.


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/elevated_button_theme.dart#L34