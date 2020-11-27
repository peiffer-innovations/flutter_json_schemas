[*description*][description]

# InkWell class #

A rectangular area of a Material that responds to touch.

For a variant of this widget that does not clip splashes, see InkResponse.

The following diagram shows how an InkWell looks when tapped, when using default values.

![The highlight is a rectangle the size of the box.][]

The InkWell widget must have a Material widget as an ancestor. The Material widget is where the ink reactions are actually painted. This matches the material design premise wherein the Material is what is actually reacting to touches by spreading ink.

If a Widget uses this class directly, it should include the following line at the top of its build function to call debugCheckHasMaterial:

    assert(debugCheckHasMaterial(context));

## Troubleshooting ##

### The ink splashes aren't visible! ###

If there is an opaque graphic, e.g. painted using a Container, Image, or DecoratedBox, between the Material widget and the InkWell widget, then the splash won't be visible because it will be under the opaque graphic. This is because ink splashes draw on the underlying Material itself, as if the ink was spreading inside the material.

The Ink widget can be used as a replacement for Image, Container, or DecoratedBox to ensure that the image or decoration also paints in the Material itself, below the ink.

If this is not possible for some reason, e.g. because you are using an opaque CustomPaint widget, alternatively consider using a second Material above the opaque widget but below the InkWell (as an ancestor to the ink well). The MaterialType.transparency material kind can be used for this purpose.

### The ink splashes don't track the size of an animated container ###

If the size of an InkWell's Material ancestor changes while the InkWell's splashes are expanding, you may notice that the splashes aren't clipped correctly. This can't be avoided.

An example of this situation is as follows:

 *link* 

Interactive App Sample code

Tap the container to cause it to grow. Then, tap it again and hold before the widget reaches its maximum size to observe the clipped ink splash.

To create a local project with this code sample, run:  
flutter create --sample=material.InkWell.1 mysample

Tap the container to cause it to grow. Then, tap it again and hold before the widget reaches its maximum size to observe the clipped ink splash.

*assignment*

    double sideLength = 50;
    
    Widget build(BuildContext context) {
      return AnimatedContainer(
        height: sideLength,
        width: sideLength,
        duration: Duration(seconds: 2),
        curve: Curves.easeIn,
        child: Material(
          color: Colors.yellow,
          child: InkWell(
            onTap: () {
              setState(() {
                sideLength == 50 ? sideLength = 100 : sideLength = 50;
              });
            },
          ),
        ),
      );
    }

An InkWell's splashes will not properly update to conform to changes if the size of its underlying Material, where the splashes are rendered, changes during animation. You should avoid using InkWells within Material widgets that are changing size.

See also:

 *  GestureDetector, for listening for gestures without ink splashes.
 *  ElevatedButton and TextButton, two kinds of buttons in material design.
 *  InkResponse, a variant of InkWell that doesn't force a rectangular shape on the ink reaction.

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatelessWidget
 *  InkResponse
 *  InkWell

## Constructors ##

InkWell(\{Key key, Widget child, GestureTapCallback onTap, GestureTapCallback onDoubleTap, GestureLongPressCallback onLongPress, void onTapDown(TapDownDetails details), GestureTapCancelCallback onTapCancel, ValueChanged<bool> onHighlightChanged, ValueChanged<bool> onHover, MouseCursor mouseCursor, Color focusColor, Color hoverColor, Color highlightColor, MaterialStateProperty<Color> overlayColor, Color splashColor, InteractiveInkFeatureFactory splashFactory, double radius, BorderRadius borderRadius, ShapeBorder customBorder, bool enableFeedback: true, bool excludeFromSemantics: false, FocusNode focusNode, bool canRequestFocus: true, ValueChanged<bool> onFocusChange, bool autofocus: false\})

Creates an ink well. \[...\]

const

## Properties ##

autofocus → bool

True if this widget will be selected as the initial focus when no other node in its scope is currently focused. \[...\]

final, inherited

borderRadius → BorderRadius

The clipping radius of the containing rect. This is effective only if customBorder is null. \[...\]

final, inherited

canRequestFocus → bool

If true, this widget may request the primary focus. \[...\]

final, inherited

child → Widget

The widget below this widget in the tree. \[...\]

final, inherited

containedInkWell → bool

Whether this ink response should be clipped its bounds. \[...\]

final, inherited

customBorder → ShapeBorder

The custom clip border which overrides borderRadius.

final, inherited

enableFeedback → bool

Whether detected gestures should provide acoustic and/or haptic feedback. \[...\]

final, inherited

excludeFromSemantics → bool

Whether to exclude the gestures introduced by this widget from the semantics tree. \[...\]

final, inherited

focusColor → Color

The color of the ink response when the parent widget is focused. If this property is null then the focus color of the theme, ThemeData.focusColor, will be used. \[...\]

final, inherited

focusNode → FocusNode

An optional focus node to use as the focus node for this widget. \[...\]

final, inherited

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

highlightColor → Color

The highlight color of the ink response when pressed. If this property is null then the highlight color of the theme, ThemeData.highlightColor, will be used. \[...\]

final, inherited

highlightShape → BoxShape

The shape (e.g., circle, rectangle) to use for the highlight drawn around this part of the material when pressed, hovered over, or focused. \[...\]

final, inherited

hoverColor → Color

The color of the ink response when a pointer is hovering over it. If this property is null then the hover color of the theme, ThemeData.hoverColor, will be used. \[...\]

final, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

mouseCursor → MouseCursor

The cursor for a mouse pointer when it enters or is hovering over the widget. \[...\]

final, inherited

onDoubleTap → GestureTapCallback

Called when the user double taps this part of the material.

final, inherited

onFocusChange → ValueChanged<bool>

Handler called when the focus changes. \[...\]

final, inherited

onHighlightChanged → ValueChanged<bool>

Called when this part of the material either becomes highlighted or stops being highlighted. \[...\]

final, inherited

onHover → ValueChanged<bool>

Called when a pointer enters or exits the ink response area. \[...\]

final, inherited

onLongPress → GestureLongPressCallback

Called when the user long-presses on this part of the material.

final, inherited

onTap → GestureTapCallback

Called when the user taps this part of the material.

final, inherited

onTapCancel → GestureTapCallback

Called when the user cancels a tap that was started on this part of the material.

final, inherited

onTapDown → void Function(TapDownDetails details)

Called when the user taps down this part of the material.

final, inherited

overlayColor → MaterialStateProperty<Color>

Defines the ink response focus, hover, and splash colors. \[...\]

final, inherited

radius → double

The radius of the ink splash. \[...\]

final, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

splashColor → Color

The splash color of the ink response. If this property is null then the splash color of the theme, ThemeData.splashColor, will be used. \[...\]

final, inherited

splashFactory → InteractiveInkFeatureFactory

Defines the appearance of the splash. \[...\]

final, inherited

## Methods ##

build(BuildContext context) → Widget

Describes the part of the user interface represented by this widget. \[...\]

inherited

createElement() → StatelessElement

Creates a StatelessElement to manage this widget's location in the tree. \[...\]

inherited

debugCheckContext(BuildContext context) → bool

Asserts that the given context satisfies the prerequisites for this class. \[...\]

@mustCallSuper, inherited

debugDescribeChildren() → List<DiagnosticsNode>

Returns a list of DiagnosticsNode objects describing this node's children. \[...\]

@protected, inherited

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

inherited

getRectCallback(RenderBox referenceBox) → RectCallback

The rectangle to use for the highlight effect and for clipping the splash effects if containedInkWell is true. \[...\]

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/ink_well.dart#L1214
[The highlight is a rectangle the size of the box.]: https://flutter.github.io/assets-for-api-docs/assets/material/ink_well.png