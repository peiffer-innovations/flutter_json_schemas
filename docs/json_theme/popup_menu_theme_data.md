[*description*][description]

# PopupMenuThemeData class #

Defines the visual properties of the routes used to display popup menus as well as PopupMenuItem and PopupMenuDivider widgets.

Descendant widgets obtain the current PopupMenuThemeData object using `PopupMenuTheme.of(context)`. Instances of PopupMenuThemeData can be customized with PopupMenuThemeData.copyWith.

Typically, a PopupMenuThemeData is specified as part of the overall Theme with ThemeData.popupMenuTheme. Otherwise, PopupMenuTheme can be used to configure its own widget subtree.

All PopupMenuThemeData properties are `null` by default. If any of these properties are null, the popup menu will provide its own defaults.

See also:

 *  ThemeData, which describes the overall theme information for the application.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

PopupMenuThemeData(\{Color color, ShapeBorder shape, double elevation, TextStyle textStyle\})

Creates the set of properties used to configure PopupMenuTheme.

const

## Properties ##

color → Color

The background color of the popup menu.

final

elevation → double

The elevation of the popup menu.

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

shape → ShapeBorder

The shape of the popup menu.

final

textStyle → TextStyle

The text style of items in the popup menu.

final

## Methods ##

copyWith(\{Color color, ShapeBorder shape, double elevation, TextStyle textStyle\}) → PopupMenuThemeData

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

lerp(PopupMenuThemeData a, PopupMenuThemeData b, double t) → PopupMenuThemeData

Linearly interpolate between two popup menu themes. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/popup_menu_theme.dart#L35