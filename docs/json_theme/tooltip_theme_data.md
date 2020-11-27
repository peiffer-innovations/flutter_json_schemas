[*description*][description]

# TooltipThemeData class #

Defines the visual properties of Tooltip widgets.

Used by TooltipTheme to control the visual properties of tooltips in a widget subtree.

To obtain this configuration, use TooltipTheme.of to access the closest ancestor TooltipTheme of the current BuildContext.

See also:

 *  TooltipTheme, an InheritedWidget that propagates the theme down its subtree.
 *  TooltipThemeData, which describes the actual configuration of a tooltip theme.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

TooltipThemeData(\{double height, EdgeInsetsGeometry padding, EdgeInsetsGeometry margin, double verticalOffset, bool preferBelow, bool excludeFromSemantics, Decoration decoration, TextStyle textStyle, Duration waitDuration, Duration showDuration\})

Creates the set of properties used to configure Tooltips.

const

## Properties ##

decoration → Decoration

The Tooltip's shape and background color.

final

excludeFromSemantics → bool

Whether the Tooltip.message should be excluded from the semantics tree. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

height → double

The height of Tooltip.child.

final

margin → EdgeInsetsGeometry

If provided, the amount of empty space to surround the Tooltip.

final

padding → EdgeInsetsGeometry

If provided, the amount of space by which to inset Tooltip.child.

final

preferBelow → bool

Whether the tooltip is displayed below its widget by default. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

showDuration → Duration

The length of time that the tooltip will be shown once it has appeared.

final

textStyle → TextStyle

The style to use for the message of Tooltips.

final

verticalOffset → double

The vertical gap between the widget and the displayed tooltip. \[...\]

final

waitDuration → Duration

The length of time that a pointer must hover over a tooltip's widget before the tooltip will be shown.

final

## Methods ##

copyWith(\{double height, EdgeInsetsGeometry padding, EdgeInsetsGeometry margin, double verticalOffset, bool preferBelow, bool excludeFromSemantics, Decoration decoration, TextStyle textStyle, Duration waitDuration, Duration showDuration\}) → TooltipThemeData

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

lerp(TooltipThemeData a, TooltipThemeData b, double t) → TooltipThemeData

Linearly interpolate between two tooltip themes. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/tooltip_theme.dart#L29