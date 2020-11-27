[*description*][description]

# BottomAppBarTheme class #

Defines default property values for descendant BottomAppBar widgets.

Descendant widgets obtain the current BottomAppBarTheme object using `BottomAppBarTheme.of(context)`. Instances of BottomAppBarTheme can be customized with BottomAppBarTheme.copyWith.

Typically a BottomAppBarTheme is specified as part of the overall Theme with ThemeData.bottomAppBarTheme.

All BottomAppBarTheme properties are `null` by default. When null, the BottomAppBar constructor provides defaults.

See also:

 *  ThemeData, which describes the overall theme information for the application.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

BottomAppBarTheme(\{Color color, double elevation, NotchedShape shape\})

Creates a theme that can be used for ThemeData.bottomAppBarTheme.

const

## Properties ##

color → Color

Default value for BottomAppBar.color. \[...\]

final

elevation → double

Default value for BottomAppBar.elevation.

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

shape → NotchedShape

Default value for BottomAppBar.shape.

final

## Methods ##

copyWith(\{Color color, double elevation, NotchedShape shape\}) → BottomAppBarTheme

Creates a copy of this object but with the given fields replaced with the new values.

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

lerp(BottomAppBarTheme a, BottomAppBarTheme b, double t) → BottomAppBarTheme

Linearly interpolate between two BAB themes. \[...\]

of(BuildContext context) → BottomAppBarTheme

The ThemeData.bottomAppBarTheme property of the ambient Theme.


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/bottom_app_bar_theme.dart#L31