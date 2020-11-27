[*description*][description]

# RaisedButton class #

A material design "raised button".

### This class is obsolete, please use ElevatedButton instead. ###

FlatButton, RaisedButton, and OutlineButton have been replaced by TextButton, ElevatedButton, and OutlinedButton respectively. ButtonTheme has been replaced by TextButtonTheme, ElevatedButtonTheme, and OutlinedButtonTheme. The original classes will be deprecated soon, please migrate code that uses them. There's a detailed migration guide for the new button and button theme classes in [flutter.dev/go/material-button-migration-guide][flutter.dev_go_material-button-migration-guide].

A raised button is based on a Material widget whose Material.elevation increases when the button is pressed.

Use raised buttons to add dimension to otherwise mostly flat layouts, e.g. in long busy lists of content, or in wide spaces. Avoid using raised buttons on already-raised content such as dialogs or cards.

If onPressed and onLongPress callbacks are null, then the button will be disabled and by default will resemble a flat button in the disabledColor. If you are trying to change the button's color and it is not having any effect, check that you are passing a non-null onPressed or onLongPress callbacks.

If you want an ink-splash effect for taps, but don't want to use a button, consider using InkWell directly.

Raised buttons have a minimum size of 88.0 by 36.0 which can be overridden with ButtonTheme.

 *link* 

Interactive App Sample code

This sample shows how to render a disabled RaisedButton, an enabled RaisedButton and lastly a RaisedButton with gradient background.

![Three raised buttons, one enabled, another disabled, and the last one styled with a blue gradient background][Three raised buttons_ one enabled_ another disabled_ and the last one styled with a blue gradient background]

To create a local project with this code sample, run:  
flutter create --sample=material.RaisedButton.1 mysample

This sample shows how to render a disabled RaisedButton, an enabled RaisedButton and lastly a RaisedButton with gradient background.

![Three raised buttons, one enabled, another disabled, and the last one styled with a blue gradient background][Three raised buttons_ one enabled_ another disabled_ and the last one styled with a blue gradient background]

*assignment*

    Widget build(BuildContext context) {
      return Center(
        child: Column(
          mainAxisSize: MainAxisSize.min,
          children: <Widget>[
            const RaisedButton(
              onPressed: null,
              child: Text(
                'Disabled Button',
                style: TextStyle(fontSize: 20)
              ),
            ),
            const SizedBox(height: 30),
            RaisedButton(
              onPressed: () {},
              child: const Text(
                'Enabled Button',
                style: TextStyle(fontSize: 20)
              ),
            ),
            const SizedBox(height: 30),
            RaisedButton(
              onPressed: () {},
              textColor: Colors.white,
              padding: const EdgeInsets.all(0.0),
              child: Container(
                decoration: const BoxDecoration(
                  gradient: LinearGradient(
                    colors: <Color>[
                      Color(0xFF0D47A1),
                      Color(0xFF1976D2),
                      Color(0xFF42A5F5),
                    ],
                  ),
                ),
                padding: const EdgeInsets.all(10.0),
                child: const Text(
                  'Gradient Button',
                  style: TextStyle(fontSize: 20)
                ),
              ),
            ),
          ],
        ),
      );
    }

See also:

 *  FlatButton, a material design button without a shadow.
 *  DropdownButton, a button that shows options to select from.
 *  FloatingActionButton, the round button in material applications.
 *  IconButton, to create buttons that just contain icons.
 *  InkWell, which implements the ink splash part of a flat button.
 *  RawMaterialButton, the widget this widget is based on.
 *  [material.io/design/components/buttons.html][material.io_design_components_buttons.html]
 *  Cookbook: [Build a form with validation][]

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatelessWidget
 *  MaterialButton
 *  RaisedButton

## Constructors ##

RaisedButton(\{Key key, @required VoidCallback onPressed, VoidCallback onLongPress, ValueChanged<bool> onHighlightChanged, MouseCursor mouseCursor, ButtonTextTheme textTheme, Color textColor, Color disabledTextColor, Color color, Color disabledColor, Color focusColor, Color hoverColor, Color highlightColor, Color splashColor, Brightness colorBrightness, double elevation, double focusElevation, double hoverElevation, double highlightElevation, double disabledElevation, EdgeInsetsGeometry padding, VisualDensity visualDensity, ShapeBorder shape, Clip clipBehavior: Clip.none, FocusNode focusNode, bool autofocus: false, MaterialTapTargetSize materialTapTargetSize, Duration animationDuration, Widget child\})

Create a filled button. \[...\]

const

RaisedButton.icon(\{Key key, @required VoidCallback onPressed, VoidCallback onLongPress, ValueChanged<bool> onHighlightChanged, MouseCursor mouseCursor, ButtonTextTheme textTheme, Color textColor, Color disabledTextColor, Color color, Color disabledColor, Color focusColor, Color hoverColor, Color highlightColor, Color splashColor, Brightness colorBrightness, double elevation, double highlightElevation, double disabledElevation, ShapeBorder shape, Clip clipBehavior, FocusNode focusNode, bool autofocus, EdgeInsetsGeometry padding, MaterialTapTargetSize materialTapTargetSize, Duration animationDuration, @required Widget icon, @required Widget label\})

Create a filled button from a pair of widgets that serve as the button's `icon` and `label`. \[...\]

factory

## Properties ##

animationDuration → Duration

Defines the duration of animated changes for shape and elevation. \[...\]

final, inherited

autofocus → bool

True if this widget will be selected as the initial focus when no other node in its scope is currently focused. \[...\]

final, inherited

child → Widget

The button's label. \[...\]

final, inherited

clipBehavior → Clip

The content will be clipped (or not) according to this option. \[...\]

final, inherited

color → Color

The button's fill color, displayed by its Material, while it is in its default (unpressed, enabled) state. \[...\]

final, inherited

colorBrightness → Brightness

The theme brightness to use for this button. \[...\]

final, inherited

disabledColor → Color

The fill color of the button when the button is disabled. \[...\]

final, inherited

disabledElevation → double

The elevation for the button's Material relative to its parent when the button is not enabled. \[...\]

final, inherited

disabledTextColor → Color

The color to use for this button's text when the button is disabled. \[...\]

final, inherited

elevation → double

The z-coordinate at which to place this button relative to its parent. \[...\]

final, inherited

enabled → bool

Whether the button is enabled or disabled. \[...\]

read-only, inherited

enableFeedback → bool

Whether detected gestures should provide acoustic and/or haptic feedback. \[...\]

final, inherited

focusColor → Color

The fill color of the button's Material when it has the input focus. \[...\]

final, inherited

focusElevation → double

The elevation for the button's Material when the button is enabled and has the input focus. \[...\]

final, inherited

focusNode → FocusNode

An optional focus node to use as the focus node for this widget. \[...\]

final, inherited

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

height → double

The vertical extent of the button. \[...\]

final, inherited

highlightColor → Color

The highlight color of the button's InkWell. \[...\]

final, inherited

highlightElevation → double

The elevation for the button's Material relative to its parent when the button is enabled and pressed. \[...\]

final, inherited

hoverColor → Color

The fill color of the button's Material when a pointer is hovering over it. \[...\]

final, inherited

hoverElevation → double

The elevation for the button's Material when the button is enabled and a pointer is hovering over it. \[...\]

final, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

materialTapTargetSize → MaterialTapTargetSize

Configures the minimum size of the tap target. \[...\]

final, inherited

minWidth → double

The smallest horizontal extent that the button will occupy. \[...\]

final, inherited

mouseCursor → MouseCursor

The cursor for a mouse pointer when it enters or is hovering over the button. \[...\]

final, inherited

onHighlightChanged → ValueChanged<bool>

Called by the underlying InkWell widget's InkWell.onHighlightChanged callback. \[...\]

final, inherited

onLongPress → VoidCallback

The callback that is called when the button is long-pressed. \[...\]

final, inherited

onPressed → VoidCallback

The callback that is called when the button is tapped or otherwise activated. \[...\]

final, inherited

padding → EdgeInsetsGeometry

The internal padding for the button's child. \[...\]

final, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

shape → ShapeBorder

The shape of the button's Material. \[...\]

final, inherited

splashColor → Color

The splash color of the button's InkWell. \[...\]

final, inherited

textColor → Color

The color to use for this button's text. \[...\]

final, inherited

textTheme → ButtonTextTheme

Defines the button's base colors, and the defaults for the button's minimum size, internal padding, and shape. \[...\]

final, inherited

visualDensity → VisualDensity

Defines how compact the button's layout will be. \[...\]

final, inherited

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/raised_button.dart#L116
[flutter.dev_go_material-button-migration-guide]: https://flutter.dev/go/material-button-migration-guide
[Three raised buttons_ one enabled_ another disabled_ and the last one styled with a blue gradient background]: https://flutter.github.io/assets-for-api-docs/assets/material/raised_button.png
[material.io_design_components_buttons.html]: https://material.io/design/components/buttons.html
[Build a form with validation]: https://flutter.dev/docs/cookbook/forms/validation