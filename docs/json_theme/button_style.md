[*description*][description]

# ButtonStyle class #

The visual properties that most buttons have in common.

Buttons and their themes have a ButtonStyle property which defines the visual properties whose default values are to be overidden. The default values are defined by the invidual button widgets and are typically based on overall theme's ThemeData.colorScheme and ThemeData.textTheme.

All of the ButtonStyle properties are null by default.

Many of the ButtonStyle properties are MaterialStateProperty objects which resolve to different values depending on the button's state. For example the Color properties are defined with `MaterialStateProperty<Color>` and can resolve to different colors depending on if the button is pressed, hovered, focused, disabled, etc.

These properties can override the default value for just one state or all of them. For example to create a ElevatedButton whose background color is the color scheme’s primary color with 50% opacity, but only when the button is pressed, one could write:

    ElevatedButton(
      style: ButtonStyle(
        backgroundColor: MaterialStateProperty.resolveWith<Color>(
          (Set<MaterialState> states) {
            if (states.contains(MaterialState.pressed))
              return Theme.of(context).colorScheme.primary.withOpacity(0.5);
            return null; // Use the component's default.
          },
        ),
      ),
    )

In this case the background color for all other button states would fallback to the ElevatedButton’s default values. To unconditionally set the button's backgroundColor for all states one could write:

    ElevatedButton(
      style: ButtonStyle(
        backgroundColor: MaterialStateProperty.all<Color>(Colors.green),
      ),
    )

Configuring a ButtonStyle directly makes it possible to very precisely control the button’s visual attributes for all states. This level of control is typically required when a custom “branded” look and feel is desirable. However, in many cases it’s useful to make relatively sweeping changes based on a few initial parameters with simple values. The button styleFrom() methods enable such sweeping changes. See for example: TextButton.styleFrom, ElevatedButton.styleFrom, OutlinedButton.styleFrom.

For example, to override the default text and icon colors for a TextButton, as well as its overlay color, with all of the standard opacity adjustments for the pressed, focused, and hovered states, one could write:

    TextButton(
      style: TextButton.styleFrom(primary: Colors.green),
    )

To configure all of the application's text buttons in the same way, specify the overall theme's `textButtonTheme`:

    MaterialApp(
      theme: ThemeData(
        textButtonTheme: TextButtonThemeData(
          style: TextButton.styleFrom(primary: Colors.green),
        ),
      ),
      home: MyAppHome(),
    )

See also:

 *  TextButtonTheme, the theme for TextButtons.
 *  ElevatedButtonTheme, the theme for ElevatedButtons.
 *  OutlinedButtonTheme, the theme for OutlinedButtons.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

ButtonStyle(\{MaterialStateProperty<TextStyle> textStyle, MaterialStateProperty<Color> backgroundColor, MaterialStateProperty<Color> foregroundColor, MaterialStateProperty<Color> overlayColor, MaterialStateProperty<Color> shadowColor, MaterialStateProperty<double> elevation, MaterialStateProperty<EdgeInsetsGeometry> padding, MaterialStateProperty<Size> minimumSize, MaterialStateProperty<BorderSide> side, MaterialStateProperty<OutlinedBorder> shape, MaterialStateProperty<MouseCursor> mouseCursor, VisualDensity visualDensity, MaterialTapTargetSize tapTargetSize, Duration animationDuration, bool enableFeedback\})

Create a ButtonStyle.

const

## Properties ##

animationDuration → Duration

Defines the duration of animated changes for shape and elevation. \[...\]

final

backgroundColor → MaterialStateProperty<Color>

The button's background fill color.

final

elevation → MaterialStateProperty<double>

The elevation of the button's Material.

final

enableFeedback → bool

Whether detected gestures should provide acoustic and/or haptic feedback. \[...\]

final

foregroundColor → MaterialStateProperty<Color>

The color for the button's Text and Icon widget descendants. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

minimumSize → MaterialStateProperty<Size>

The minimum size of the button itself. \[...\]

final

mouseCursor → MaterialStateProperty<MouseCursor>

The cursor for a mouse pointer when it enters or is hovering over this button's InkWell.

final

overlayColor → MaterialStateProperty<Color>

The highlight color that's typically used to indicate that the button is focused, hovered, or pressed.

final

padding → MaterialStateProperty<EdgeInsetsGeometry>

The padding between the button's boundary and its child.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

shadowColor → MaterialStateProperty<Color>

The shadow color of the button's Material. \[...\]

final

shape → MaterialStateProperty<OutlinedBorder>

The shape of the button's underlying Material. \[...\]

final

side → MaterialStateProperty<BorderSide>

The color and weight of the button's outline. \[...\]

final

tapTargetSize → MaterialTapTargetSize

Configures the minimum size of the area within which the button may be pressed. \[...\]

final

textStyle → MaterialStateProperty<TextStyle>

The style for a button's Text widget descendants. \[...\]

final

visualDensity → VisualDensity

Defines how compact the button's layout will be. \[...\]

final

## Methods ##

copyWith(\{MaterialStateProperty<TextStyle> textStyle, MaterialStateProperty<Color> backgroundColor, MaterialStateProperty<Color> foregroundColor, MaterialStateProperty<Color> overlayColor, MaterialStateProperty<Color> shadowColor, MaterialStateProperty<double> elevation, MaterialStateProperty<EdgeInsetsGeometry> padding, MaterialStateProperty<Size> minimumSize, MaterialStateProperty<BorderSide> side, MaterialStateProperty<OutlinedBorder> shape, MaterialStateProperty<MouseCursor> mouseCursor, VisualDensity visualDensity, MaterialTapTargetSize tapTargetSize, Duration animationDuration, bool enableFeedback\}) → ButtonStyle

Returns a copy of this ButtonStyle with the given fields replaced with the new values.

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

override

merge(ButtonStyle style) → ButtonStyle

Returns a copy of this ButtonStyle where the non-null fields in `style` have replaced the corresponding null fields in this ButtonStyle. \[...\]

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

lerp(ButtonStyle a, ButtonStyle b, double t) → ButtonStyle

Linearly interpolate between two ButtonStyles.


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/button_style.dart#L101