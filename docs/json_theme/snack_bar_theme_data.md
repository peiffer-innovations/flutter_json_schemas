[*description*][description]

# SnackBarThemeData class #

Customizes default property values for SnackBar widgets.

Descendant widgets obtain the current SnackBarThemeData object using `Theme.of(context).snackBarTheme`. Instances of SnackBarThemeData can be customized with SnackBarThemeData.copyWith.

Typically a SnackBarThemeData is specified as part of the overall Theme with ThemeData.snackBarTheme. The default for ThemeData.snackBarTheme provides all `null` properties.

All SnackBarThemeData properties are `null` by default. When null, the SnackBar will provide its own defaults.

See also:

 *  ThemeData, which describes the overall theme information for the application.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

SnackBarThemeData(\{Color backgroundColor, Color actionTextColor, Color disabledActionTextColor, TextStyle contentTextStyle, double elevation, ShapeBorder shape, SnackBarBehavior behavior\})

Creates a theme that can be used for ThemeData.snackBarTheme. \[...\]

const

## Properties ##

actionTextColor → Color

Default value for SnackBarAction.textColor. \[...\]

final

backgroundColor → Color

Default value for SnackBar.backgroundColor. \[...\]

final

behavior → SnackBarBehavior

Default value for SnackBar.behavior. \[...\]

final

contentTextStyle → TextStyle

Used to configure the DefaultTextStyle for the SnackBar.content widget. \[...\]

final

disabledActionTextColor → Color

Default value for SnackBarAction.disabledTextColor. \[...\]

final

elevation → double

Default value for SnackBar.elevation. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

shape → ShapeBorder

Default value for SnackBar.shape. \[...\]

final

## Methods ##

copyWith(\{Color backgroundColor, Color actionTextColor, Color disabledActionTextColor, TextStyle contentTextStyle, double elevation, ShapeBorder shape, SnackBarBehavior behavior\}) → SnackBarThemeData

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

lerp(SnackBarThemeData a, SnackBarThemeData b, double t) → SnackBarThemeData

Linearly interpolate between two SnackBar Themes. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/snack_bar_theme.dart#L52