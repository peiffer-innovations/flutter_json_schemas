[*description*][description]

# AppBarTheme class #

Defines default property values for descendant AppBar widgets.

Descendant widgets obtain the current AppBarTheme object using `AppBarTheme.of(context)`. Instances of AppBarTheme can be customized with AppBarTheme.copyWith.

Typically an AppBarTheme is specified as part of the overall Theme with ThemeData.appBarTheme.

All AppBarTheme properties are `null` by default. When null, the AppBar will use the values from ThemeData if they exist, otherwise it will provide its own defaults.

See also:

 *  ThemeData, which describes the overall theme information for the application.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

AppBarTheme(\{Brightness brightness, Color color, double elevation, Color shadowColor, IconThemeData iconTheme, IconThemeData actionsIconTheme, TextTheme textTheme, bool centerTitle\})

Creates a theme that can be used for ThemeData.appBarTheme.

const

## Properties ##

actionsIconTheme → IconThemeData

Default value for AppBar.actionsIconTheme. \[...\]

final

brightness → Brightness

Default value for AppBar.brightness. \[...\]

final

centerTitle → bool

Default value for AppBar.centerTitle. \[...\]

final

color → Color

Default value for AppBar.backgroundColor. \[...\]

final

elevation → double

Default value for AppBar.elevation. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

iconTheme → IconThemeData

Default value for AppBar.iconTheme. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

shadowColor → Color

Default value for AppBar.shadowColor. \[...\]

final

textTheme → TextTheme

Default value for AppBar.textTheme. \[...\]

final

## Methods ##

copyWith(\{IconThemeData actionsIconTheme, Brightness brightness, Color color, double elevation, Color shadowColor, IconThemeData iconTheme, TextTheme textTheme, bool centerTitle\}) → AppBarTheme

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

lerp(AppBarTheme a, AppBarTheme b, double t) → AppBarTheme

Linearly interpolate between two AppBar themes. \[...\]

of(BuildContext context) → AppBarTheme

The ThemeData.appBarTheme property of the ambient Theme.


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/app_bar_theme.dart#L33