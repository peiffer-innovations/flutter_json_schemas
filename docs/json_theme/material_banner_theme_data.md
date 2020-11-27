[*description*][description]

# MaterialBannerThemeData class #

Defines the visual properties of MaterialBanner widgets.

Descendant widgets obtain the current MaterialBannerThemeData object using `MaterialBannerTheme.of(context)`. Instances of MaterialBannerThemeData can be customized with MaterialBannerThemeData.copyWith.

Typically a MaterialBannerThemeData is specified as part of the overall Theme with ThemeData.bannerTheme.

All MaterialBannerThemeData properties are `null` by default. When null, the MaterialBanner will provide its own defaults.

See also:

 *  ThemeData, which describes the overall theme information for the application.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

MaterialBannerThemeData(\{Color backgroundColor, TextStyle contentTextStyle, EdgeInsetsGeometry padding, EdgeInsetsGeometry leadingPadding\})

Creates a theme that can be used for MaterialBannerTheme or ThemeData.bannerTheme.

const

## Properties ##

backgroundColor → Color

The background color of a MaterialBanner.

final

contentTextStyle → TextStyle

Used to configure the DefaultTextStyle for the MaterialBanner.content widget.

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

leadingPadding → EdgeInsetsGeometry

The amount of space by which to inset MaterialBanner.leading.

final

padding → EdgeInsetsGeometry

The amount of space by which to inset MaterialBanner.content.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

copyWith(\{Color backgroundColor, TextStyle contentTextStyle, EdgeInsetsGeometry padding, EdgeInsetsGeometry leadingPadding\}) → MaterialBannerThemeData

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

lerp(MaterialBannerThemeData a, MaterialBannerThemeData b, double t) → MaterialBannerThemeData

Linearly interpolate between two Banner themes. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/banner_theme.dart#L29