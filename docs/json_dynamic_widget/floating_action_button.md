[*description*][description]

# FloatingActionButton class #

A material design floating action button.

A floating action button is a circular icon button that hovers over content to promote a primary action in the application. Floating action buttons are most commonly used in the Scaffold.floatingActionButton field.

Use at most a single floating action button per screen. Floating action buttons should be used for positive actions such as "create", "share", or "navigate". (If more than one floating action button is used within a Route, then make sure that each button has a unique heroTag, otherwise an exception will be thrown.)

If the onPressed callback is null, then the button will be disabled and will not react to touch. It is highly discouraged to disable a floating action button as there is no indication to the user that the button is disabled. Consider changing the backgroundColor if disabling the floating action button.

 *link* 

Interactive App Sample code

This example shows how to display a FloatingActionButton in a Scaffold, with a pink backgroundColor and a thumbs up Icon.

![floating_action_button.png][]

To create a local project with this code sample, run:  
flutter create --sample=material.FloatingActionButton.1 mysample

This example shows how to display a FloatingActionButton in a Scaffold, with a pink backgroundColor and a thumbs up Icon.

![floating_action_button.png][]

*assignment*

    Widget build(BuildContext context) {
      return Scaffold(
        appBar: AppBar(
          title: const Text('Floating Action Button'),
        ),
        body: Center(
          child: const Text('Press the button below!')
        ),
        floatingActionButton: FloatingActionButton(
          onPressed: () {
            // Add your onPressed code here!
          },
          child: Icon(Icons.navigation),
          backgroundColor: Colors.green,
        ),
      );
    }

 *link* 

Interactive App Sample code

This example shows how to make an extended FloatingActionButton in a Scaffold, with a pink backgroundColor, a thumbs up Icon and a Text label that reads "Approve".

![floating_action_button_label.png][]

To create a local project with this code sample, run:  
flutter create --sample=material.FloatingActionButton.2 mysample

This example shows how to make an extended FloatingActionButton in a Scaffold, with a pink backgroundColor, a thumbs up Icon and a Text label that reads "Approve".

![floating_action_button_label.png][]

*assignment*

    Widget build(BuildContext context) {
      return Scaffold(
        appBar: AppBar(
          title: const Text('Floating Action Button Label'),
        ),
        body: Center(
          child: const Text('Press the button with a label below!'),
        ),
        floatingActionButton: FloatingActionButton.extended(
          onPressed: () {
            // Add your onPressed code here!
          },
          label: Text('Approve'),
          icon: Icon(Icons.thumb_up),
          backgroundColor: Colors.pink,
        ),
      );
    }

See also:

 *  Scaffold, in which floating action buttons typically live.
 *  RaisedButton, another kind of button that appears to float above the content.
 *  [material.io/design/components/buttons-floating-action-button.html][material.io_design_components_buttons-floating-action-button.html]

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatelessWidget
 *  FloatingActionButton

## Constructors ##

FloatingActionButton(\{Key key, Widget child, String tooltip, Color foregroundColor, Color backgroundColor, Color focusColor, Color hoverColor, Color splashColor, Object heroTag: const \_DefaultHeroTag(), double elevation, double focusElevation, double hoverElevation, double highlightElevation, double disabledElevation, @required VoidCallback onPressed, MouseCursor mouseCursor, bool mini: false, ShapeBorder shape, Clip clipBehavior: Clip.none, FocusNode focusNode, bool autofocus: false, MaterialTapTargetSize materialTapTargetSize, bool isExtended: false\})

Creates a circular floating action button. \[...\]

const

FloatingActionButton.extended(\{Key key, String tooltip, Color foregroundColor, Color backgroundColor, Color focusColor, Color hoverColor, Object heroTag: const \_DefaultHeroTag(), double elevation, double focusElevation, double hoverElevation, Color splashColor, double highlightElevation, double disabledElevation, @required VoidCallback onPressed, MouseCursor mouseCursor: SystemMouseCursors.click, ShapeBorder shape, bool isExtended: true, MaterialTapTargetSize materialTapTargetSize, Clip clipBehavior: Clip.none, FocusNode focusNode, bool autofocus: false, Widget icon, @required Widget label\})

Creates a wider StadiumBorder\-shaped floating action button with an optional `icon` and a `label`. \[...\]

## Properties ##

autofocus → bool

True if this widget will be selected as the initial focus when no other node in its scope is currently focused. \[...\]

final

backgroundColor → Color

The button's background color. \[...\]

final

child → Widget

The widget below this widget in the tree. \[...\]

final

clipBehavior → Clip

The content will be clipped (or not) according to this option. \[...\]

final

disabledElevation → double

The z-coordinate at which to place this button when the button is disabled (onPressed is null). \[...\]

final

elevation → double

The z-coordinate at which to place this button relative to its parent. \[...\]

final

focusColor → Color

The color to use for filling the button when the button has input focus. \[...\]

final

focusElevation → double

The z-coordinate at which to place this button relative to its parent when the button has the input focus. \[...\]

final

focusNode → FocusNode

An optional focus node to use as the focus node for this widget. \[...\]

final

foregroundColor → Color

The default foreground color for icons and text within the button. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

heroTag → Object

The tag to apply to the button's Hero widget. \[...\]

final

highlightElevation → double

The z-coordinate at which to place this button relative to its parent when the user is touching the button. \[...\]

final

hoverColor → Color

The color to use for filling the button when the button has a pointer hovering over it. \[...\]

final

hoverElevation → double

The z-coordinate at which to place this button relative to its parent when the button is enabled and has a pointer hovering over it. \[...\]

final

isExtended → bool

True if this is an "extended" floating action button. \[...\]

final

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

materialTapTargetSize → MaterialTapTargetSize

Configures the minimum size of the tap target. \[...\]

final

mini → bool

Controls the size of this button. \[...\]

final

mouseCursor → MouseCursor

The cursor for a mouse pointer when it enters or is hovering over the button. \[...\]

final

onPressed → VoidCallback

The callback that is called when the button is tapped or otherwise activated. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

shape → ShapeBorder

The shape of the button's Material. \[...\]

final

splashColor → Color

The splash color for this FloatingActionButton's InkWell. \[...\]

final

tooltip → String

Text that describes the action that will occur when the button is pressed. \[...\]

final

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/floating_action_button.dart#L125
[floating_action_button.png]: https://flutter.github.io/assets-for-api-docs/assets/material/floating_action_button.png
[floating_action_button_label.png]: https://flutter.github.io/assets-for-api-docs/assets/material/floating_action_button_label.png
[material.io_design_components_buttons-floating-action-button.html]: https://material.io/design/components/buttons-floating-action-button.html