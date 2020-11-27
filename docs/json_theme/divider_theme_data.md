[*description*][description]

# DividerThemeData class #

Defines the visual properties of Divider, VerticalDivider, dividers between ListTiles, and dividers between rows in DataTables.

Descendant widgets obtain the current DividerThemeData object using `DividerTheme.of(context)`. Instances of DividerThemeData can be customized with DividerThemeData.copyWith.

Typically a DividerThemeData is specified as part of the overall Theme with ThemeData.dividerTheme.

All DividerThemeData properties are `null` by default. When null, the widgets will provide their own defaults.

See also:

 *  ThemeData, which describes the overall theme information for the application.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

DividerThemeData(\{Color color, double space, double thickness, double indent, double endIndent\})

Creates a theme that can be used for DividerTheme or ThemeData.dividerTheme.

const

## Properties ##

color → Color

The color of Dividers and VerticalDividers, also used between ListTiles, between rows in DataTables, and so forth.

final

endIndent → double

The amount of empty space at the trailing edge of Divider or bottom edge of VerticalDivider.

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

indent → double

The amount of empty space at the leading edge of Divider or top edge of VerticalDivider.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

space → double

The Divider's width or the VerticalDivider's height. \[...\]

final

thickness → double

The thickness of the line drawn within the divider.

final

## Methods ##

copyWith(\{Color color, double space, double thickness, double indent, double endIndent\}) → DividerThemeData

Creates a copy of this object with the given fields replaced with the new values.

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

lerp(DividerThemeData a, DividerThemeData b, double t) → DividerThemeData

Linearly interpolate between two Divider themes. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/divider_theme.dart#L32