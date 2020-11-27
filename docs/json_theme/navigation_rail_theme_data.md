[*description*][description]

# NavigationRailThemeData class #

Defines default property values for descendant NavigationRail widgets.

Descendant widgets obtain the current NavigationRailThemeData object using `NavigationRailTheme.of(context)`. Instances of NavigationRailThemeData can be customized with NavigationRailThemeData.copyWith.

Typically a NavigationRailThemeData is specified as part of the overall Theme with ThemeData.navigationRailTheme.

All NavigationRailThemeData properties are `null` by default. When null, the NavigationRail will use the values from ThemeData if they exist, otherwise it will provide its own defaults based on the overall Theme's textTheme and colorScheme. See the individual NavigationRail properties for details.

See also:

 *  ThemeData, which describes the overall theme information for the application.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

NavigationRailThemeData(\{Color backgroundColor, double elevation, TextStyle unselectedLabelTextStyle, TextStyle selectedLabelTextStyle, IconThemeData unselectedIconTheme, IconThemeData selectedIconTheme, double groupAlignment, NavigationRailLabelType labelType\})

Creates a theme that can be used for ThemeData.navigationRailTheme.

const

## Properties ##

backgroundColor → Color

Color to be used for the NavigationRail's background.

final

elevation → double

The z-coordinate to be used for the NavigationRail's elevation.

final

groupAlignment → double

The alignment for the NavigationRailDestinations as they are positioned within the NavigationRail.

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

labelType → NavigationRailLabelType

The type that defines the layout and behavior of the labels in the NavigationRail.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

selectedIconTheme → IconThemeData

The theme to merge with the default icon theme for NavigationRailDestination icons, when the destination is selected.

final

selectedLabelTextStyle → TextStyle

The style to merge with the default text style for NavigationRailDestination labels, when the destination is selected.

final

unselectedIconTheme → IconThemeData

The theme to merge with the default icon theme for NavigationRailDestination icons, when the destination is not selected.

final

unselectedLabelTextStyle → TextStyle

The style to merge with the default text style for NavigationRailDestination labels, when the destination is not selected.

final

## Methods ##

copyWith(\{Color backgroundColor, double elevation, TextStyle unselectedLabelTextStyle, TextStyle selectedLabelTextStyle, IconThemeData unselectedIconTheme, IconThemeData selectedIconTheme, double groupAlignment, NavigationRailLabelType labelType\}) → NavigationRailThemeData

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

lerp(NavigationRailThemeData a, NavigationRailThemeData b, double t) → NavigationRailThemeData

Linearly interpolate between two navigation rail themes. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/navigation_rail_theme.dart#L39