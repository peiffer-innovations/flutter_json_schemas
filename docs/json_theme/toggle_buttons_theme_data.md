[*description*][description]

# ToggleButtonsThemeData class #

Defines the color and border properties of ToggleButtons widgets.

Used by ToggleButtonsTheme to control the color and border properties of toggle buttons in a widget subtree.

To obtain the current ToggleButtonsTheme, use ToggleButtonsTheme.of.

Values specified here are used for ToggleButtons properties that are not given an explicit non-null value.

See also:

 *  ToggleButtonsTheme, which describes the actual configuration of a toggle buttons theme.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

ToggleButtonsThemeData(\{TextStyle textStyle, BoxConstraints constraints, Color color, Color selectedColor, Color disabledColor, Color fillColor, Color focusColor, Color highlightColor, Color hoverColor, Color splashColor, Color borderColor, Color selectedBorderColor, Color disabledBorderColor, BorderRadius borderRadius, double borderWidth\})

Creates the set of color and border properties used to configure ToggleButtons.

const

## Properties ##

borderColor → Color

The border color to display when the toggle button is enabled.

final

borderRadius → BorderRadius

The radii of the border's corners.

final

borderWidth → double

The width of the border surrounding each toggle button. \[...\]

final

color → Color

The color for descendant Text and Icon widgets if the toggle button is enabled.

final

constraints → BoxConstraints

Defines the button's size. \[...\]

final

disabledBorderColor → Color

The border color to display when the toggle button is disabled.

final

disabledColor → Color

The color for descendant Text and Icon widgets if the toggle button is disabled.

final

fillColor → Color

The fill color for selected toggle buttons.

final

focusColor → Color

The color to use for filling the button when the button has input focus.

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

highlightColor → Color

The highlight color for the toggle button's InkWell.

final

hoverColor → Color

The color to use for filling the toggle button when the button has a pointer hovering over it.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

selectedBorderColor → Color

The border color to display when the toggle button is selected.

final

selectedColor → Color

The color for descendant Text and Icon widgets if the toggle button is selected.

final

splashColor → Color

The splash color for the toggle button's InkWell.

final

textStyle → TextStyle

The default text style for ToggleButtons.children. \[...\]

final

## Methods ##

copyWith(\{TextStyle textStyle, BoxConstraints constraints, Color color, Color selectedColor, Color disabledColor, Color fillColor, Color focusColor, Color highlightColor, Color hoverColor, Color splashColor, Color borderColor, Color selectedBorderColor, Color disabledBorderColor, BorderRadius borderRadius, double borderWidth\}) → ToggleButtonsThemeData

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

lerp(ToggleButtonsThemeData a, ToggleButtonsThemeData b, double t) → ToggleButtonsThemeData

Linearly interpolate between two toggle buttons themes.


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/toggle_buttons_theme.dart#L30