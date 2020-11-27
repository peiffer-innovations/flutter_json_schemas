[*description*][description]

# Checkbox class #

A material design checkbox.

The checkbox itself does not maintain any state. Instead, when the state of the checkbox changes, the widget calls the onChanged callback. Most widgets that use a checkbox will listen for the onChanged callback and rebuild the checkbox with a new value to update the visual appearance of the checkbox.

The checkbox can optionally display three values - true, false, and null - if tristate is true. When value is null a dash is displayed. By default tristate is false and the checkbox's value must be true or false.

Requires one of its ancestors to be a Material widget.

See also:

 *  CheckboxListTile, which combines this widget with a ListTile so that you can give the checkbox a label.
 *  Switch, a widget with semantics similar to Checkbox.
 *  Radio, for selecting among a set of explicit values.
 *  Slider, for selecting a value in a range.
 *  [material.io/design/components/selection-controls.html\#checkboxes][material.io_design_components_selection-controls.html_checkboxes]
 *  [material.io/design/components/lists.html\#types][material.io_design_components_lists.html_types]

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatefulWidget
 *  Checkbox

## Constructors ##

Checkbox(\{Key key, @required bool value, bool tristate: false, @required ValueChanged<bool> onChanged, MouseCursor mouseCursor, Color activeColor, Color checkColor, Color focusColor, Color hoverColor, MaterialTapTargetSize materialTapTargetSize, VisualDensity visualDensity, FocusNode focusNode, bool autofocus: false\})

Creates a material design checkbox. \[...\]

const

## Properties ##

activeColor → Color

The color to use when this checkbox is checked. \[...\]

final

autofocus → bool

True if this widget will be selected as the initial focus when no other node in its scope is currently focused. \[...\]

final

checkColor → Color

The color to use for the check icon when this checkbox is checked. \[...\]

final

focusColor → Color

The color for the checkbox's Material when it has the input focus.

final

focusNode → FocusNode

An optional focus node to use as the focus node for this widget. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

hoverColor → Color

The color for the checkbox's Material when a pointer is hovering over it.

final

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

materialTapTargetSize → MaterialTapTargetSize

Configures the minimum size of the tap target. \[...\]

final

mouseCursor → MouseCursor

The cursor for a mouse pointer when it enters or is hovering over the widget. \[...\]

final

onChanged → ValueChanged<bool>

Called when the value of the checkbox should change. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

tristate → bool

If true the checkbox's value can be true, false, or null. \[...\]

final

value → bool

Whether this checkbox is checked. \[...\]

final

visualDensity → VisualDensity

Defines how compact the checkbox's layout will be. \[...\]

final

## Methods ##

createElement() → StatefulElement

Creates a StatefulElement to manage this widget's location in the tree. \[...\]

inherited

createState() → \_CheckboxState

Creates the mutable state for this widget at a given location in the tree. \[...\]

override

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

## Constants ##

width → const double

The width of a checkbox widget.

`18.0`


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/checkbox.dart#L44
[material.io_design_components_selection-controls.html_checkboxes]: https://material.io/design/components/selection-controls.html#checkboxes
[material.io_design_components_lists.html_types]: https://material.io/design/components/lists.html#types