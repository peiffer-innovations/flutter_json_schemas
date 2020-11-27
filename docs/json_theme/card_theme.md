[*description*][description]

# CardTheme class #

Defines default property values for descendant Card widgets.

Descendant widgets obtain the current CardTheme object using `CardTheme.of(context)`. Instances of CardTheme can be customized with CardTheme.copyWith.

Typically a CardTheme is specified as part of the overall Theme with ThemeData.cardTheme.

All CardTheme properties are `null` by default. When null, the Card will use the values from ThemeData if they exist, otherwise it will provide its own defaults.

See also:

 *  ThemeData, which describes the overall theme information for the application.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

CardTheme(\{Clip clipBehavior, Color color, Color shadowColor, double elevation, EdgeInsetsGeometry margin, ShapeBorder shape\})

Creates a theme that can be used for ThemeData.cardTheme. \[...\]

const

## Properties ##

clipBehavior → Clip

Default value for Card.clipBehavior. \[...\]

final

color → Color

Default value for Card.color. \[...\]

final

elevation → double

Default value for Card.elevation. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

margin → EdgeInsetsGeometry

Default value for Card.margin. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

shadowColor → Color

Default value for Card.shadowColor. \[...\]

final

shape → ShapeBorder

Default value for Card.shape. \[...\]

final

## Methods ##

copyWith(\{Clip clipBehavior, Color color, Color shadowColor, double elevation, EdgeInsetsGeometry margin, ShapeBorder shape\}) → CardTheme

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

lerp(CardTheme a, CardTheme b, double t) → CardTheme

Linearly interpolate between two Card themes. \[...\]

of(BuildContext context) → CardTheme

The ThemeData.cardTheme property of the ambient Theme.


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/card_theme.dart#L32