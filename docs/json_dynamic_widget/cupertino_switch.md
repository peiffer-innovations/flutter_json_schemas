[*description*][description]

# CupertinoSwitch class #

An iOS-style switch.

Used to toggle the on/off state of a single setting.

The switch itself does not maintain any state. Instead, when the state of the switch changes, the widget calls the onChanged callback. Most widgets that use a switch will listen for the onChanged callback and rebuild the switch with a new value to update the visual appearance of the switch.

 *link* 

Sample

This sample shows how to use a CupertinoSwitch in a ListTile. The MergeSemantics is used to turn the entire ListTile into a single item for accessibility tools.

*assignment*

    MergeSemantics(
      child: ListTile(
        title: Text('Lights'),
        trailing: CupertinoSwitch(
          value: _lights,
          onChanged: (bool value) { setState(() { _lights = value; }); },
        ),
        onTap: () { setState(() { _lights = !_lights; }); },
      ),
    )

See also:

 *  Switch, the material design equivalent.
 *  [developer.apple.com/ios/human-interface-guidelines/controls/switches/][developer.apple.com_ios_human-interface-guidelines_controls_switches]

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatefulWidget
 *  CupertinoSwitch

## Constructors ##

CupertinoSwitch(\{Key key, @required bool value, @required ValueChanged<bool> onChanged, Color activeColor, Color trackColor, DragStartBehavior dragStartBehavior: DragStartBehavior.start\})

Creates an iOS-style switch. \[...\]

const

## Properties ##

activeColor → Color

The color to use when this switch is on. \[...\]

final

dragStartBehavior → DragStartBehavior

Determines the way that drag start behavior is handled. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

onChanged → ValueChanged<bool>

Called when the user toggles with switch on or off. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

trackColor → Color

The color to use for the background when the switch is off. \[...\]

final

value → bool

Whether this switch is on or off. \[...\]

final

## Methods ##

createElement() → StatefulElement

Creates a StatefulElement to manage this widget's location in the tree. \[...\]

inherited

createState() → \_CupertinoSwitchState

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/cupertino/switch.dart#L55
[developer.apple.com_ios_human-interface-guidelines_controls_switches]: https://developer.apple.com/ios/human-interface-guidelines/controls/switches/