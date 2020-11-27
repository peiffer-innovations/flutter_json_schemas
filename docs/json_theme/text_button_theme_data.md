[*description*][description]

# TextButtonThemeData class #

A ButtonStyle that overrides the default appearance of TextButtons when it's used with TextButtonTheme or with the overall Theme's ThemeData.textButtonTheme.

The style's properties override TextButton's default style, i.e. the ButtonStyle returned by TextButton.defaultStyleOf. Only the style's non-null property values or resolved non-null MaterialStateProperty values are used.

See also:

 *  TextButtonTheme, the theme which is configured with this class.
 *  TextButton.defaultStyleOf, which returns the default ButtonStyle for text buttons.
 *  TextButton.styleFrom, which converts simple values into a ButtonStyle that's consistent with TextButton's defaults.
 *  MaterialStateProperty.resolve, "resolve" a material state property to a simple value based on a set of MaterialStates.
 *  ThemeData.textButtonTheme, which can be used to override the default ButtonStyle for TextButtons below the overall Theme.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

TextButtonThemeData(\{ButtonStyle style\})

Creates a TextButtonThemeData. \[...\]

const

## Properties ##

hashCode → int

The hash code for this object. \[...\]

read-only, override

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

style → ButtonStyle

Overrides for TextButton's default style. \[...\]

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

lerp(TextButtonThemeData a, TextButtonThemeData b, double t) → TextButtonThemeData

Linearly interpolate between two text button themes.


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/text_button_theme.dart#L34