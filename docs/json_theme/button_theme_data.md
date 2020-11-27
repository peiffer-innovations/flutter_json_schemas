[*description*][description]

# ButtonThemeData class #

Used with ButtonTheme to configure the color and geometry of buttons.

### This class is obsolete. ###

Please use one or more of the new buttons and their themes instead:

 *  TextButton, TextButtonTheme, TextButtonThemeData,
 *  ElevatedButton, ElevatedButtonTheme, ElevatedButtonThemeData,
 *  OutlinedButton, OutlinedButtonTheme, OutlinedButtonThemeData

FlatButton, RaisedButton, and OutlineButton have been replaced by TextButton, ElevatedButton, and OutlinedButton respectively. ButtonTheme has been replaced by TextButtonTheme, ElevatedButtonTheme, and OutlinedButtonTheme. The original classes will be deprecated soon, please migrate code that uses them. There's a detailed migration guide for the new button and button theme classes in [flutter.dev/go/material-button-migration-guide][flutter.dev_go_material-button-migration-guide].

A button theme can be specified as part of the overall Material theme using ThemeData.buttonTheme. The Material theme's button theme data can be overridden with ButtonTheme.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

ButtonThemeData(\{ButtonTextTheme textTheme: ButtonTextTheme.normal, double minWidth: 88.0, double height: 36.0, EdgeInsetsGeometry padding, ShapeBorder shape, ButtonBarLayoutBehavior layoutBehavior: ButtonBarLayoutBehavior.padded, bool alignedDropdown: false, Color buttonColor, Color disabledColor, Color focusColor, Color hoverColor, Color highlightColor, Color splashColor, ColorScheme colorScheme, MaterialTapTargetSize materialTapTargetSize\})

Create a button theme object that can be used with ButtonTheme or ThemeData. \[...\]

const

## Properties ##

alignedDropdown → bool

If true, then a DropdownButton menu's width will match the button's width. \[...\]

final

colorScheme → ColorScheme

A set of thirteen colors that can be used to derive the button theme's colors. \[...\]

final

constraints → BoxConstraints

Simply a convenience that returns minWidth and height as a BoxConstraints object: \[...\]

read-only

hashCode → int

The hash code for this object. \[...\]

read-only, override

height → double

The minimum height for buttons. \[...\]

final

layoutBehavior → ButtonBarLayoutBehavior

Defines whether a ButtonBar should size itself with a minimum size constraint or with padding. \[...\]

final

minWidth → double

The minimum width for buttons. \[...\]

final

padding → EdgeInsetsGeometry

Padding for a button's child (typically the button's label). \[...\]

read-only

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

shape → ShapeBorder

The shape of a button's material. \[...\]

read-only

textTheme → ButtonTextTheme

Defines a button's base colors, and the defaults for the button's minimum size, internal padding, and shape. \[...\]

final

## Methods ##

copyWith(\{ButtonTextTheme textTheme, ButtonBarLayoutBehavior layoutBehavior, double minWidth, double height, EdgeInsetsGeometry padding, ShapeBorder shape, bool alignedDropdown, Color buttonColor, Color disabledColor, Color focusColor, Color hoverColor, Color highlightColor, Color splashColor, ColorScheme colorScheme, MaterialTapTargetSize materialTapTargetSize\}) → ButtonThemeData

Creates a copy of this button theme data object with the matching fields replaced with the non-null parameter values.

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

override

getAnimationDuration(MaterialButton button) → Duration

The duration of the `button`'s highlight animation. \[...\]

getBrightness(MaterialButton button) → Brightness

The `button`'s overall brightness. \[...\]

getConstraints(MaterialButton button) → BoxConstraints

The BoxConstraints that the define the `button`'s size. \[...\]

getDisabledElevation(MaterialButton button) → double

The `button`'s elevation when MaterialButton.onPressed is null (when MaterialButton.enabled is false). \[...\]

getDisabledFillColor(MaterialButton button) → Color

The `button`'s background color when MaterialButton.onPressed is null (when MaterialButton.enabled is false). \[...\]

getDisabledTextColor(MaterialButton button) → Color

The foreground color of the `button`'s text and icon when MaterialButton.onPressed is null (when MaterialButton.enabled is false). \[...\]

getElevation(MaterialButton button) → double

The `button`'s elevation when it is enabled and has not been pressed. \[...\]

getFillColor(MaterialButton button) → Color

The button's background fill color or null for buttons that don't have a background color. \[...\]

getFocusColor(MaterialButton button) → Color

The fill color of the button when it has input focus. \[...\]

getFocusElevation(MaterialButton button) → double

The `button`'s elevation when it is enabled and has focus. \[...\]

getHighlightColor(MaterialButton button) → Color

The color of the overlay that appears when the `button` is pressed. \[...\]

getHighlightElevation(MaterialButton button) → double

The `button`'s elevation when it is enabled and has been pressed. \[...\]

getHoverColor(MaterialButton button) → Color

The fill color of the button when it has input focus. \[...\]

getHoverElevation(MaterialButton button) → double

The `button`'s elevation when it is enabled and has focus. \[...\]

getMaterialTapTargetSize(MaterialButton button) → MaterialTapTargetSize

The minimum size of the `button`'s tap target. \[...\]

getPadding(MaterialButton button) → EdgeInsetsGeometry

Padding for the `button`'s child (typically the button's label). \[...\]

getShape(MaterialButton button) → ShapeBorder

The shape of the `button`'s Material. \[...\]

getSplashColor(MaterialButton button) → Color

The color of the ink "splash" overlay that appears when the (enabled) `button` is tapped. \[...\]

getTextColor(MaterialButton button) → Color

The foreground color of the `button`'s text and icon. \[...\]

getTextTheme(MaterialButton button) → ButtonTextTheme

Defines the `button`'s base colors, and the defaults for the button's minimum size, internal padding, and shape. \[...\]

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/button_theme.dart#L277
[flutter.dev_go_material-button-migration-guide]: https://flutter.dev/go/material-button-migration-guide