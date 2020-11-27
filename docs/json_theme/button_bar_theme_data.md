[*description*][description]

# ButtonBarThemeData class #

Defines the visual properties of ButtonBar widgets.

Used by ButtonBarTheme to control the visual properties of ButtonBar instances in a widget subtree.

To obtain this configuration, use ButtonBarTheme.of to access the closest ancestor ButtonBarTheme of the current BuildContext.

See also:

 *  ButtonBarTheme, an InheritedWidget that propagates the theme down its subtree.
 *  ButtonBar, which uses this to configure itself and its children button widgets.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

ButtonBarThemeData(\{MainAxisAlignment alignment, MainAxisSize mainAxisSize, ButtonTextTheme buttonTextTheme, double buttonMinWidth, double buttonHeight, EdgeInsetsGeometry buttonPadding, bool buttonAlignedDropdown, ButtonBarLayoutBehavior layoutBehavior, VerticalDirection overflowDirection\})

Constructs the set of properties used to configure ButtonBar widgets. \[...\]

const

## Properties ##

alignment → MainAxisAlignment

How the children should be placed along the horizontal axis.

final

buttonAlignedDropdown → bool

If true, then a DropdownButton menu's width will match the ButtonBar button's width. \[...\]

final

buttonHeight → double

The minimum height for ButtonBar buttons. \[...\]

final

buttonMinWidth → double

The minimum width for ButtonBar buttons. \[...\]

final

buttonPadding → EdgeInsetsGeometry

Padding for a ButtonBar button's child (typically the button's label). \[...\]

final

buttonTextTheme → ButtonTextTheme

Defines a ButtonBar button's base colors, and the defaults for the button's minimum size, internal padding, and shape. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

layoutBehavior → ButtonBarLayoutBehavior

Defines whether a ButtonBar should size itself with a minimum size constraint or with padding.

final

mainAxisSize → MainAxisSize

How much horizontal space is available. See Row.mainAxisSize.

final

overflowDirection → VerticalDirection

Defines the vertical direction of a ButtonBar's children if it overflows. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

copyWith(\{MainAxisAlignment alignment, MainAxisSize mainAxisSize, ButtonTextTheme buttonTextTheme, double buttonMinWidth, double buttonHeight, EdgeInsetsGeometry buttonPadding, bool buttonAlignedDropdown, ButtonBarLayoutBehavior layoutBehavior, VerticalDirection overflowDirection\}) → ButtonBarThemeData

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

lerp(ButtonBarThemeData a, ButtonBarThemeData b, double t) → ButtonBarThemeData

Linearly interpolate between two button bar themes. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/button_bar_theme.dart#L30