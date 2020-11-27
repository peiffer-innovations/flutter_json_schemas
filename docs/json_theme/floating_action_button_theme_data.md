[*description*][description]

# FloatingActionButtonThemeData class #

Defines default property values for descendant FloatingActionButton widgets.

Descendant widgets obtain the current FloatingActionButtonThemeData object using `Theme.of(context).floatingActionButtonTheme`. Instances of FloatingActionButtonThemeData can be customized with FloatingActionButtonThemeData.copyWith.

Typically a FloatingActionButtonThemeData is specified as part of the overall Theme with ThemeData.floatingActionButtonTheme.

All FloatingActionButtonThemeData properties are `null` by default. When null, the FloatingActionButton will use the values from ThemeData if they exist, otherwise it will provide its own defaults.

See also:

 *  ThemeData, which describes the overall theme information for the application.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

FloatingActionButtonThemeData(\{Color foregroundColor, Color backgroundColor, Color focusColor, Color hoverColor, Color splashColor, double elevation, double focusElevation, double hoverElevation, double disabledElevation, double highlightElevation, ShapeBorder shape\})

Creates a theme that can be used for ThemeData.floatingActionButtonTheme.

const

## Properties ##

backgroundColor → Color

Color to be used for the unselected, enabled FloatingActionButton's background.

final

disabledElevation → double

The z-coordinate to be used for the disabled FloatingActionButton's elevation foreground.

final

elevation → double

The z-coordinate to be used for the unselected, enabled FloatingActionButton's elevation foreground.

final

focusColor → Color

The color to use for filling the button when the button has input focus.

final

focusElevation → double

The z-coordinate at which to place this button relative to its parent when the button has the input focus. \[...\]

final

foregroundColor → Color

Color to be used for the unselected, enabled FloatingActionButton's foreground.

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

highlightElevation → double

The z-coordinate to be used for the selected, enabled FloatingActionButton's elevation foreground.

final

hoverColor → Color

The color to use for filling the button when the button has a pointer hovering over it.

final

hoverElevation → double

The z-coordinate at which to place this button relative to its parent when the button is enabled and has a pointer hovering over it. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

shape → ShapeBorder

The shape to be used for the floating action button's Material.

final

splashColor → Color

The splash color for this FloatingActionButton's InkWell.

final

## Methods ##

copyWith(\{Color foregroundColor, Color backgroundColor, Color focusColor, Color hoverColor, Color splashColor, double elevation, double focusElevation, double hoverElevation, double disabledElevation, double highlightElevation, ShapeBorder shape\}) → FloatingActionButtonThemeData

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

lerp(FloatingActionButtonThemeData a, FloatingActionButtonThemeData b, double t) → FloatingActionButtonThemeData

Linearly interpolate between two floating action button themes. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/floating_action_button_theme.dart#L32