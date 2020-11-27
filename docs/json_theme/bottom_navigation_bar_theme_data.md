[*description*][description]

# BottomNavigationBarThemeData class #

Defines default property values for descendant BottomNavigationBar widgets.

Descendant widgets obtain the current BottomNavigationBarThemeData object using `BottomNavigationBarTheme.of(context)`. Instances of BottomNavigationBarThemeData can be customized with BottomNavigationBarThemeData.copyWith.

Typically a BottomNavigationBarThemeData is specified as part of the overall Theme with ThemeData.bottomNavigationBarTheme.

All BottomNavigationBarThemeData properties are `null` by default. When null, the BottomNavigationBar's build method provides defaults.

See also:

 *  ThemeData, which describes the overall theme information for the application.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

BottomNavigationBarThemeData(\{Color backgroundColor, double elevation, IconThemeData selectedIconTheme, IconThemeData unselectedIconTheme, Color selectedItemColor, Color unselectedItemColor, TextStyle selectedLabelStyle, TextStyle unselectedLabelStyle, bool showSelectedLabels, bool showUnselectedLabels, BottomNavigationBarType type\})

Creates a theme that can be used for ThemeData.bottomNavigationBarTheme.

const

## Properties ##

backgroundColor → Color

The color of the BottomNavigationBar itself. \[...\]

final

elevation → double

The z-coordinate of the BottomNavigationBar. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

selectedIconTheme → IconThemeData

The size, opacity, and color of the icon in the currently selected BottomNavigationBarItem.icon. \[...\]

final

selectedItemColor → Color

The color of the selected BottomNavigationBarItem.icon and BottomNavigationBarItem.title. \[...\]

final

selectedLabelStyle → TextStyle

The TextStyle of the BottomNavigationBarItem labels when they are selected. \[...\]

final

showSelectedLabels → bool

Whether the labels are shown for the unselected BottomNavigationBarItems. \[...\]

final

showUnselectedLabels → bool

Whether the labels are shown for the selected BottomNavigationBarItem. \[...\]

final

type → BottomNavigationBarType

Defines the layout and behavior of a BottomNavigationBar. \[...\]

final

unselectedIconTheme → IconThemeData

The size, opacity, and color of the icon in the currently unselected BottomNavigationBarItem.icons. \[...\]

final

unselectedItemColor → Color

The color of the unselected BottomNavigationBarItem.icon and BottomNavigationBarItem.titles. \[...\]

final

unselectedLabelStyle → TextStyle

The TextStyle of the BottomNavigationBarItem labels when they are not selected. \[...\]

final

## Methods ##

copyWith(\{Color backgroundColor, double elevation, IconThemeData selectedIconTheme, IconThemeData unselectedIconTheme, Color selectedItemColor, Color unselectedItemColor, TextStyle selectedLabelStyle, TextStyle unselectedLabelStyle, bool showSelectedLabels, bool showUnselectedLabels, BottomNavigationBarType type\}) → BottomNavigationBarThemeData

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

lerp(BottomNavigationBarThemeData a, BottomNavigationBarThemeData b, double t) → BottomNavigationBarThemeData

Linearly interpolate between two BottomNavigationBarThemeData. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/bottom_navigation_bar_theme.dart#L34