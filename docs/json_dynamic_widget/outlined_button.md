[*description*][description]

# OutlinedButton class #

A Material Design "Outlined Button"; essentially a TextButton with an outlined border.

Outlined buttons are medium-emphasis buttons. They contain actions that are important, but they aren’t the primary action in an app.

An outlined button is a label child displayed on a (zero elevation) Material widget. The label's Text and Icon widgets are displayed in the style's ButtonStyle.foregroundColor and the outline's weight and color are defined by ButtonStyle.side. The button reacts to touches by filling with the style's ButtonStyle.backgroundColor.

The outlined button's default style is defined by defaultStyleOf. The style of this outline button can be overridden with its style parameter. The style of all text buttons in a subtree can be overridden with the OutlinedButtonTheme and the style of all of the outlined buttons in an app can be overridden with the Theme's ThemeData.outlinedButtonTheme property.

The static styleFrom method is a convenient way to create a outlined button ButtonStyle from simple values.

See also:

 *  ElevatedButton, a filled material design button with a shadow.
 *  TextButton, a material design button without a shadow.
 *  [material.io/design/components/buttons.html][material.io_design_components_buttons.html]

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatefulWidget
 *  ButtonStyleButton
 *  OutlinedButton

## Constructors ##

OutlinedButton(\{Key key, @required VoidCallback onPressed, VoidCallback onLongPress, ButtonStyle style, FocusNode focusNode, bool autofocus: false, Clip clipBehavior: Clip.none, @required Widget child\})

Create an OutlinedButton. \[...\]

const

OutlinedButton.icon(\{Key key, @required VoidCallback onPressed, VoidCallback onLongPress, ButtonStyle style, FocusNode focusNode, bool autofocus, Clip clipBehavior, @required Widget icon, @required Widget label\})

Create a text button from a pair of widgets that serve as the button's `icon` and `label`. \[...\]

factory

## Properties ##

autofocus → bool

True if this widget will be selected as the initial focus when no other node in its scope is currently focused. \[...\]

final, inherited

child → Widget

Typically the button's label.

final, inherited

clipBehavior → Clip

The content will be clipped (or not) according to this option. \[...\]

final, inherited

enabled → bool

Whether the button is enabled or disabled. \[...\]

read-only, inherited

focusNode → FocusNode

An optional focus node to use as the focus node for this widget. \[...\]

final, inherited

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

onLongPress → VoidCallback

Called when the button is long-pressed. \[...\]

final, inherited

onPressed → VoidCallback

Called when the button is tapped or otherwise activated. \[...\]

final, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

style → ButtonStyle

Customizes this button's appearance. \[...\]

final, inherited

## Methods ##

createElement() → StatefulElement

Creates a StatefulElement to manage this widget's location in the tree. \[...\]

inherited

createState() → \_ButtonStyleState

Creates the mutable state for this widget at a given location in the tree. \[...\]

inherited

debugDescribeChildren() → List<DiagnosticsNode>

Returns a list of DiagnosticsNode objects describing this node's children. \[...\]

@protected, inherited

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

inherited

defaultStyleOf(BuildContext context) → ButtonStyle

Defines the button's default appearance. \[...\]

override

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

themeStyleOf(BuildContext context) → ButtonStyle

Returns the ButtonStyle that belongs to the button's component theme. \[...\]

override

toDiagnosticsNode(\{String name, DiagnosticsTreeStyle style\}) → DiagnosticsNode

Returns a debug representation of the object that is used by debugging tools and by DiagnosticsNode.toStringDeep. \[...\]

inherited

toString(\{DiagnosticLevel minLevel: DiagnosticLevel.info\}) → String

Returns a string representation of this object.

inherited

toStringDeep(\{String prefixLineOne: '', String prefixOtherLines, DiagnosticLevel minLevel: DiagnosticLevel.debug\}) → String

Returns a string representation of this node and its descendants. \[...\]

inherited

toStringShallow(\{String joiner: ', ', DiagnosticLevel minLevel: DiagnosticLevel.debug\}) → String

Returns a one-line detailed description of the object. \[...\]

inherited

toStringShort() → String

A short, textual description of this widget.

inherited

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

@nonVirtual, inherited

## Static Methods ##

styleFrom(\{Color primary, Color onSurface, Color backgroundColor, Color shadowColor, double elevation, TextStyle textStyle, EdgeInsetsGeometry padding, Size minimumSize, BorderSide side, OutlinedBorder shape, MouseCursor enabledMouseCursor, MouseCursor disabledMouseCursor, VisualDensity visualDensity, MaterialTapTargetSize tapTargetSize, Duration animationDuration, bool enableFeedback\}) → ButtonStyle

A static convenience method that constructs an outlined button ButtonStyle given simple values. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/outlined_button.dart#L52
[material.io_design_components_buttons.html]: https://material.io/design/components/buttons.html