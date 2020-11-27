[*description*][description]

# IconThemeData class #

Defines the color, opacity, and size of icons.

Used by IconTheme to control the color, opacity, and size of icons in a widget subtree.

To obtain the current icon theme, use IconTheme.of. To convert an icon theme to a version with all the fields filled in, use new IconThemeData.fallback.

Mixed in types

 *  Diagnosticable

Implementers

 *  CupertinoIconThemeData

Annotations

 *  @immutable

## Constructors ##

IconThemeData(\{Color color, double opacity, double size\})

Creates an icon theme data. \[...\]

const

IconThemeData.fallback()

Creates an icon them with some reasonable default values. \[...\]

const

## Properties ##

color → Color

The default color for icons.

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

isConcrete → bool

Whether all the properties of this object are non-null.

read-only

opacity → double

An opacity to apply to both explicit and default icon colors.

read-only

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

size → double

The default size for icons.

final

## Methods ##

copyWith(\{Color color, double opacity, double size\}) → IconThemeData

Creates a copy of this icon theme but with the given fields replaced with the new values.

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

override

merge(IconThemeData other) → IconThemeData

Returns a new icon theme that matches this icon theme but with some values replaced by the non-null parameters of the given icon theme. If the given icon theme is null, simply returns this icon theme.

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

resolve(BuildContext context) → IconThemeData

Called by IconTheme.of to convert this instance to an IconThemeData that fits the given BuildContext. \[...\]

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

lerp(IconThemeData a, IconThemeData b, double t) → IconThemeData

Linearly interpolate between two icon theme data objects. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/icon_theme_data.dart#L24