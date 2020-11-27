[*description*][description]

# Radio<T> class #

A material design radio button.

Used to select between a number of mutually exclusive values. When one radio button in a group is selected, the other radio buttons in the group cease to be selected. The values are of type `T`, the type parameter of the Radio class. Enums are commonly used for this purpose.

The radio button itself does not maintain any state. Instead, selecting the radio invokes the onChanged callback, passing value as a parameter. If groupValue and value match, this radio will be selected. Most widgets will respond to onChanged by calling State.setState to update the radio button's groupValue.

 *link* 

Interactive App Sample code

Here is an example of Radio widgets wrapped in ListTiles, which is similar to what you could get with the RadioListTile widget.

The currently selected character is passed into `groupValue`, which is maintained by the example's `State`. In this case, the first `Radio` will start off selected because `_character` is initialized to `SingingCharacter.lafayette`.

If the second radio button is pressed, the example's state is updated with `setState`, updating `_character` to `SingingCharacter.jefferson`. This causes the buttons to rebuild with the updated `groupValue`, and therefore the selection of the second button.

Requires one of its ancestors to be a Material widget.

To create a local project with this code sample, run:  
flutter create --sample=material.Radio.1 mysample

Here is an example of Radio widgets wrapped in ListTiles, which is similar to what you could get with the RadioListTile widget.

The currently selected character is passed into `groupValue`, which is maintained by the example's `State`. In this case, the first `Radio` will start off selected because `_character` is initialized to `SingingCharacter.lafayette`.

If the second radio button is pressed, the example's state is updated with `setState`, updating `_character` to `SingingCharacter.jefferson`. This causes the buttons to rebuild with the updated `groupValue`, and therefore the selection of the second button.

Requires one of its ancestors to be a Material widget.

*assignment*

    enum SingingCharacter { lafayette, jefferson }
    
    // ...
    
    SingingCharacter _character = SingingCharacter.lafayette;
    
    Widget build(BuildContext context) {
      return Column(
        children: <Widget>[
          ListTile(
            title: const Text('Lafayette'),
            leading: Radio(
              value: SingingCharacter.lafayette,
              groupValue: _character,
              onChanged: (SingingCharacter value) {
                setState(() { _character = value; });
              },
            ),
          ),
          ListTile(
            title: const Text('Thomas Jefferson'),
            leading: Radio(
              value: SingingCharacter.jefferson,
              groupValue: _character,
              onChanged: (SingingCharacter value) {
                setState(() { _character = value; });
              },
            ),
          ),
        ],
      );
    }

See also:

 *  RadioListTile, which combines this widget with a ListTile so that you can give the radio button a label.
 *  Slider, for selecting a value in a range.
 *  Checkbox and Switch, for toggling a particular value on or off.
 *  [material.io/design/components/selection-controls.html\#radio-buttons][material.io_design_components_selection-controls.html_radio-buttons]

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatefulWidget
 *  Radio

## Constructors ##

Radio(\{Key key, @required T value, @required T groupValue, @required ValueChanged<T> onChanged, MouseCursor mouseCursor, bool toggleable: false, Color activeColor, Color focusColor, Color hoverColor, MaterialTapTargetSize materialTapTargetSize, VisualDensity visualDensity, FocusNode focusNode, bool autofocus: false\})

Creates a material design radio button. \[...\]

const

## Properties ##

activeColor → Color

The color to use when this radio button is selected. \[...\]

final

autofocus → bool

True if this widget will be selected as the initial focus when no other node in its scope is currently focused. \[...\]

final

focusColor → Color

The color for the radio's Material when it has the input focus.

final

focusNode → FocusNode

An optional focus node to use as the focus node for this widget. \[...\]

final

groupValue → T

The currently selected value for a group of radio buttons. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

hoverColor → Color

The color for the radio's Material when a pointer is hovering over it.

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

onChanged → ValueChanged<T>

Called when the user selects this radio button. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

toggleable → bool

Set to true if this radio button is allowed to be returned to an indeterminate state by selecting it again when selected. \[...\]

final

value → T

The value represented by this radio button.

final

visualDensity → VisualDensity

Defines how compact the radio's layout will be. \[...\]

final

## Methods ##

createElement() → StatefulElement

Creates a StatefulElement to manage this widget's location in the tree. \[...\]

inherited

createState() → \_RadioState<T>

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/radio.dart#L95
[material.io_design_components_selection-controls.html_radio-buttons]: https://material.io/design/components/selection-controls.html#radio-buttons