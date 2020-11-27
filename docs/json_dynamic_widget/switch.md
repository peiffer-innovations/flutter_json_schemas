[*description*][description]

# Switch class #

A material design switch.

Used to toggle the on/off state of a single setting.

The switch itself does not maintain any state. Instead, when the state of the switch changes, the widget calls the onChanged callback. Most widgets that use a switch will listen for the onChanged callback and rebuild the switch with a new value to update the visual appearance of the switch.

If the onChanged callback is null, then the switch will be disabled (it will not respond to input). A disabled switch's thumb and track are rendered in shades of grey by default. The default appearance of a disabled switch can be overridden with inactiveThumbColor and inactiveTrackColor.

Requires one of its ancestors to be a Material widget.

See also:

 *  SwitchListTile, which combines this widget with a ListTile so that you can give the switch a label.
 *  Checkbox, another widget with similar semantics.
 *  Radio, for selecting among a set of explicit values.
 *  Slider, for selecting a value in a range.
 *  [material.io/design/components/selection-controls.html\#switches][material.io_design_components_selection-controls.html_switches]

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatefulWidget
 *  Switch

## Constructors ##

Switch(\{Key key, @required bool value, @required ValueChanged<bool> onChanged, Color activeColor, Color activeTrackColor, Color inactiveThumbColor, Color inactiveTrackColor, ImageProvider<Object> activeThumbImage, void onActiveThumbImageError(dynamic exception, StackTrace stackTrace), ImageProvider<Object> inactiveThumbImage, void onInactiveThumbImageError(dynamic exception, StackTrace stackTrace), MaterialTapTargetSize materialTapTargetSize, DragStartBehavior dragStartBehavior: DragStartBehavior.start, MouseCursor mouseCursor, Color focusColor, Color hoverColor, FocusNode focusNode, bool autofocus: false\})

Creates a material design switch. \[...\]

const

Switch.adaptive(\{Key key, @required bool value, @required ValueChanged<bool> onChanged, Color activeColor, Color activeTrackColor, Color inactiveThumbColor, Color inactiveTrackColor, ImageProvider<Object> activeThumbImage, void onActiveThumbImageError(dynamic exception, StackTrace stackTrace), ImageProvider<Object> inactiveThumbImage, void onInactiveThumbImageError(dynamic exception, StackTrace stackTrace), MaterialTapTargetSize materialTapTargetSize, DragStartBehavior dragStartBehavior: DragStartBehavior.start, MouseCursor mouseCursor, Color focusColor, Color hoverColor, FocusNode focusNode, bool autofocus: false\})

Creates a CupertinoSwitch if the target platform is iOS, creates a material design switch otherwise. \[...\]

const

## Properties ##

activeColor → Color

The color to use when this switch is on. \[...\]

final

activeThumbImage → ImageProvider<Object>

An image to use on the thumb of this switch when the switch is on. \[...\]

final

activeTrackColor → Color

The color to use on the track when this switch is on. \[...\]

final

autofocus → bool

True if this widget will be selected as the initial focus when no other node in its scope is currently focused. \[...\]

final

dragStartBehavior → DragStartBehavior

Determines the way that drag start behavior is handled. \[...\]

final

focusColor → Color

The color for the button's Material when it has the input focus.

final

focusNode → FocusNode

An optional focus node to use as the focus node for this widget. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

hoverColor → Color

The color for the button's Material when a pointer is hovering over it.

final

inactiveThumbColor → Color

The color to use on the thumb when this switch is off. \[...\]

final

inactiveThumbImage → ImageProvider<Object>

An image to use on the thumb of this switch when the switch is off. \[...\]

final

inactiveTrackColor → Color

The color to use on the track when this switch is off. \[...\]

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

onActiveThumbImageError → void Function(dynamic exception, StackTrace stackTrace)

An optional error callback for errors emitted when loading activeThumbImage.

final

onChanged → ValueChanged<bool>

Called when the user toggles the switch on or off. \[...\]

final

onInactiveThumbImageError → void Function(dynamic exception, StackTrace stackTrace)

An optional error callback for errors emitted when loading inactiveThumbImage.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

value → bool

Whether this switch is on or off. \[...\]

final

## Methods ##

createElement() → StatefulElement

Creates a StatefulElement to manage this widget's location in the tree. \[...\]

inherited

createState() → \_SwitchState

Creates the mutable state for this widget at a given location in the tree. \[...\]

override

debugDescribeChildren() → List<DiagnosticsNode>

Returns a list of DiagnosticsNode objects describing this node's children. \[...\]

@protected, inherited

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/switch.dart#L56
[material.io_design_components_selection-controls.html_switches]: https://material.io/design/components/selection-controls.html#switches