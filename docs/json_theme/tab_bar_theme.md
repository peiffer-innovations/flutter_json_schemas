[*description*][description]

# TabBarTheme class #

Defines a theme for TabBar widgets.

A tab bar theme describes the color of the tab label and the size/shape of the TabBar.indicator.

Descendant widgets obtain the current theme's TabBarTheme object using `TabBarTheme.of(context)`. Instances of TabBarTheme can be customized with TabBarTheme.copyWith.

See also:

 *  TabBar, a widget that displays a horizontal row of tabs.
 *  ThemeData, which describes the overall theme information for the application.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

TabBarTheme(\{Decoration indicator, TabBarIndicatorSize indicatorSize, Color labelColor, EdgeInsetsGeometry labelPadding, TextStyle labelStyle, Color unselectedLabelColor, TextStyle unselectedLabelStyle\})

Creates a tab bar theme that can be used with ThemeData.tabBarTheme.

const

## Properties ##

hashCode → int

The hash code for this object. \[...\]

read-only, override

indicator → Decoration

Default value for TabBar.indicator.

final

indicatorSize → TabBarIndicatorSize

Default value for TabBar.indicatorSize.

final

labelColor → Color

Default value for TabBar.labelColor.

final

labelPadding → EdgeInsetsGeometry

Default value for TabBar.labelPadding.

final

labelStyle → TextStyle

Default value for TabBar.labelStyle.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

unselectedLabelColor → Color

Default value for TabBar.unselectedLabelColor.

final

unselectedLabelStyle → TextStyle

Default value for TabBar.unselectedLabelStyle.

final

## Methods ##

copyWith(\{Decoration indicator, TabBarIndicatorSize indicatorSize, Color labelColor, EdgeInsetsGeometry labelPadding, TextStyle labelStyle, Color unselectedLabelColor, TextStyle unselectedLabelStyle\}) → TabBarTheme

Creates a copy of this object but with the given fields replaced with the new values.

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

@mustCallSuper, @protected, inherited

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

lerp(TabBarTheme a, TabBarTheme b, double t) → TabBarTheme

Linearly interpolate between two tab bar themes. \[...\]

of(BuildContext context) → TabBarTheme

The data from the closest TabBarTheme instance given the build context.


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/tab_bar_theme.dart#L29