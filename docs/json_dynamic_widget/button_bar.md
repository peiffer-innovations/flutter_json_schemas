[*description*][description]

# ButtonBar class #

An end-aligned row of buttons, laying out into a column if there is not enough horizontal space.

Places the buttons horizontally according to the buttonPadding. The children are laid out in a Row with MainAxisAlignment.end. When the Directionality is TextDirection.ltr, the button bar's children are right justified and the last child becomes the rightmost child. When the Directionality TextDirection.rtl the children are left justified and the last child becomes the leftmost child.

If the button bar's width exceeds the maximum width constraint on the widget, it aligns its buttons in a column. The key difference here is that the MainAxisAlignment will then be treated as a cross-axis/horizontal alignment. For example, if the buttons overflow and ButtonBar.alignment was set to MainAxisAlignment.start, the buttons would align to the horizontal start of the button bar.

The ButtonBar can be configured with a ButtonBarTheme. For any null property on the ButtonBar, the surrounding ButtonBarTheme's property will be used instead. If the ButtonBarTheme's property is null as well, the property will default to a value described in the field documentation below.

The children are wrapped in a ButtonTheme that is a copy of the surrounding ButtonTheme with the button properties overridden by the properties of the ButtonBar as described above. These properties include buttonTextTheme, buttonMinWidth, buttonHeight, buttonPadding, and buttonAlignedDropdown.

Used by Dialog to arrange the actions at the bottom of the dialog.

See also:

 *  RaisedButton, a kind of button.
 *  FlatButton, another kind of button.
 *  Card, at the bottom of which it is common to place a ButtonBar.
 *  Dialog, which uses a ButtonBar for its actions.
 *  ButtonBarTheme, which configures the ButtonBar.

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatelessWidget
 *  ButtonBar

## Constructors ##

ButtonBar(\{Key key, MainAxisAlignment alignment, MainAxisSize mainAxisSize, ButtonTextTheme buttonTextTheme, double buttonMinWidth, double buttonHeight, EdgeInsetsGeometry buttonPadding, bool buttonAlignedDropdown, ButtonBarLayoutBehavior layoutBehavior, VerticalDirection overflowDirection, double overflowButtonSpacing, List<Widget> children: const <Widget>\[\]\})

Creates a button bar. \[...\]

const

## Properties ##

alignment → MainAxisAlignment

How the children should be placed along the horizontal axis. \[...\]

final

buttonAlignedDropdown → bool

Overrides the surrounding ButtonThemeData.alignedDropdown to define whether a DropdownButton menu's width will match the button's width. \[...\]

final

buttonHeight → double

Overrides the surrounding ButtonThemeData.height to define a button's minimum height. \[...\]

final

buttonMinWidth → double

Overrides the surrounding ButtonThemeData.minWidth to define a button's minimum width. \[...\]

final

buttonPadding → EdgeInsetsGeometry

Overrides the surrounding ButtonThemeData.padding to define the padding for a button's child (typically the button's label). \[...\]

final

buttonTextTheme → ButtonTextTheme

Overrides the surrounding ButtonBarThemeData.buttonTextTheme to define a button's base colors, size, internal padding and shape. \[...\]

final

children → List<Widget>

The buttons to arrange horizontally. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

layoutBehavior → ButtonBarLayoutBehavior

Defines whether a ButtonBar should size itself with a minimum size constraint or with padding. \[...\]

final

mainAxisSize → MainAxisSize

How much horizontal space is available. See Row.mainAxisSize. \[...\]

final

overflowButtonSpacing → double

The spacing between buttons when the button bar overflows. \[...\]

final

overflowDirection → VerticalDirection

Defines the vertical direction of a ButtonBar's children if it overflows. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

build(BuildContext context) → Widget

Describes the part of the user interface represented by this widget. \[...\]

override

createElement() → StatelessElement

Creates a StatelessElement to manage this widget's location in the tree. \[...\]

inherited

debugDescribeChildren() → List<DiagnosticsNode>

Returns a list of DiagnosticsNode objects describing this node's children. \[...\]

@protected, inherited

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

inherited

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/button_bar.dart#L54