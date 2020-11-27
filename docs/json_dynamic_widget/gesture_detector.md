[*description*][description]

# GestureDetector class #

A widget that detects gestures.

Attempts to recognize gestures that correspond to its non-null callbacks.

If this widget has a child, it defers to that child for its sizing behavior. If it does not have a child, it grows to fit the parent instead.

By default a GestureDetector with an invisible child ignores touches; this behavior can be controlled with behavior.

GestureDetector also listens for accessibility events and maps them to the callbacks. To ignore accessibility events, set excludeFromSemantics to true.

See [flutter.dev/gestures/][flutter.dev_gestures] for additional information.

Material design applications typically react to touches with ink splash effects. The InkWell class implements this effect and can be used in place of a GestureDetector for handling taps.

 *link* 

Sample

This example of a Container contains a black light bulb wrapped in a GestureDetector. It turns the light bulb yellow when the "turn lights on" button is tapped by setting the `_lights` field. Above animation shows the code in use:

*assignment*

    Container(
      alignment: FractionalOffset.center,
      color: Colors.white,
      child: Column(
        mainAxisAlignment: MainAxisAlignment.center,
        children: <Widget>[
          Padding(
            padding: const EdgeInsets.all(8.0),
            child: Icon(
              Icons.lightbulb_outline,
              color: _lights ? Colors.yellow.shade600 : Colors.black,
              size: 60,
            ),
          ),
          GestureDetector(
            onTap: () {
              setState(() {
                _lights = true;
              });
            },
            child: Container(
              color: Colors.yellow.shade600,
              padding: const EdgeInsets.all(8),
              child: const Text('TURN LIGHTS ON'),
            ),
          ),
        ],
      ),
    )

 *link* 

Sample

This example of a Container wraps a GestureDetector widget. Since the GestureDetector does not have a child it takes on the size of its parent making the entire area of the surrounding Container clickable. When tapped the Container turns yellow by setting the `_color` field:

*assignment*

    Container(
      color: _color,
      height: 200.0,
      width: 200.0,
      child: GestureDetector(
        onTap: () {
          setState(() {
            _color = Colors.yellow;
          });
        },
      ),
    )

## Debugging ##

To see how large the hit test box of a GestureDetector is for debugging purposes, set debugPaintPointersEnabled to true.

See also:

 *  Listener, a widget for listening to lower-level raw pointer events.
 *  MouseRegion, a widget that tracks the movement of mice, even when no button is pressed.

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatelessWidget
 *  GestureDetector

## Constructors ##

GestureDetector(\{Key key, Widget child, void onTapDown(TapDownDetails details), void onTapUp(TapUpDetails details), GestureTapCallback onTap, GestureTapCancelCallback onTapCancel, GestureTapCallback onSecondaryTap, void onSecondaryTapDown(TapDownDetails details), void onSecondaryTapUp(TapUpDetails details), GestureTapCancelCallback onSecondaryTapCancel, void onTertiaryTapDown(TapDownDetails details), void onTertiaryTapUp(TapUpDetails details), GestureTapCancelCallback onTertiaryTapCancel, void onDoubleTapDown(TapDownDetails details), GestureTapCallback onDoubleTap, GestureTapCancelCallback onDoubleTapCancel, GestureLongPressCallback onLongPress, void onLongPressStart(LongPressStartDetails details), void onLongPressMoveUpdate(LongPressMoveUpdateDetails details), GestureLongPressUpCallback onLongPressUp, void onLongPressEnd(LongPressEndDetails details), GestureLongPressCallback onSecondaryLongPress, void onSecondaryLongPressStart(LongPressStartDetails details), void onSecondaryLongPressMoveUpdate(LongPressMoveUpdateDetails details), GestureLongPressUpCallback onSecondaryLongPressUp, void onSecondaryLongPressEnd(LongPressEndDetails details), void onVerticalDragDown(DragDownDetails details), void onVerticalDragStart(DragStartDetails details), void onVerticalDragUpdate(DragUpdateDetails details), void onVerticalDragEnd(DragEndDetails details), GestureDragCancelCallback onVerticalDragCancel, void onHorizontalDragDown(DragDownDetails details), void onHorizontalDragStart(DragStartDetails details), void onHorizontalDragUpdate(DragUpdateDetails details), void onHorizontalDragEnd(DragEndDetails details), GestureDragCancelCallback onHorizontalDragCancel, void onForcePressStart(ForcePressDetails details), void onForcePressPeak(ForcePressDetails details), void onForcePressUpdate(ForcePressDetails details), void onForcePressEnd(ForcePressDetails details), void onPanDown(DragDownDetails details), void onPanStart(DragStartDetails details), void onPanUpdate(DragUpdateDetails details), void onPanEnd(DragEndDetails details), GestureDragCancelCallback onPanCancel, void onScaleStart(ScaleStartDetails details), void onScaleUpdate(ScaleUpdateDetails details), void onScaleEnd(ScaleEndDetails details), HitTestBehavior behavior, bool excludeFromSemantics: false, DragStartBehavior dragStartBehavior: DragStartBehavior.start\})

Creates a widget that detects gestures. \[...\]

## Properties ##

behavior → HitTestBehavior

How this gesture detector should behave during hit testing. \[...\]

final

child → Widget

The widget below this widget in the tree. \[...\]

final

dragStartBehavior → DragStartBehavior

Determines the way that drag start behavior is handled. \[...\]

final

excludeFromSemantics → bool

Whether to exclude these gestures from the semantics tree. For example, the long-press gesture for showing a tooltip is excluded because the tooltip itself is included in the semantics tree directly and so having a gesture to show it would result in duplication of information.

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

onDoubleTap → GestureTapCallback

The user has tapped the screen with a primary button at the same location twice in quick succession. \[...\]

final

onDoubleTapCancel → GestureTapCancelCallback

The pointer that previously triggered onDoubleTapDown will not end up causing a double tap. \[...\]

final

onDoubleTapDown → void Function(TapDownDetails details)

A pointer that might cause a double tap has contacted the screen at a particular location. \[...\]

final

onForcePressEnd → void Function(ForcePressDetails details)

The pointer is no longer in contact with the screen. \[...\]

final

onForcePressPeak → void Function(ForcePressDetails details)

The pointer is in contact with the screen and has pressed with the maximum force. The amount of force is at least ForcePressGestureRecognizer.peakPressure. \[...\]

final

onForcePressStart → void Function(ForcePressDetails details)

The pointer is in contact with the screen and has pressed with sufficient force to initiate a force press. The amount of force is at least ForcePressGestureRecognizer.startPressure. \[...\]

final

onForcePressUpdate → void Function(ForcePressDetails details)

A pointer is in contact with the screen, has previously passed the ForcePressGestureRecognizer.startPressure and is either moving on the plane of the screen, pressing the screen with varying forces or both simultaneously. \[...\]

final

onHorizontalDragCancel → GestureDragCancelCallback

The pointer that previously triggered onHorizontalDragDown did not complete. \[...\]

final

onHorizontalDragDown → void Function(DragDownDetails details)

A pointer has contacted the screen with a primary button and might begin to move horizontally. \[...\]

final

onHorizontalDragEnd → void Function(DragEndDetails details)

A pointer that was previously in contact with the screen with a primary button and moving horizontally is no longer in contact with the screen and was moving at a specific velocity when it stopped contacting the screen. \[...\]

final

onHorizontalDragStart → void Function(DragStartDetails details)

A pointer has contacted the screen with a primary button and has begun to move horizontally. \[...\]

final

onHorizontalDragUpdate → void Function(DragUpdateDetails details)

A pointer that is in contact with the screen with a primary button and moving horizontally has moved in the horizontal direction. \[...\]

final

onLongPress → GestureLongPressCallback

Called when a long press gesture with a primary button has been recognized. \[...\]

final

onLongPressEnd → void Function(LongPressEndDetails details)

A pointer that has triggered a long-press with a primary button has stopped contacting the screen. \[...\]

final

onLongPressMoveUpdate → void Function(LongPressMoveUpdateDetails details)

A pointer has been drag-moved after a long press with a primary button. \[...\]

final

onLongPressStart → void Function(LongPressStartDetails details)

Called when a long press gesture with a primary button has been recognized. \[...\]

final

onLongPressUp → GestureLongPressUpCallback

A pointer that has triggered a long-press with a primary button has stopped contacting the screen. \[...\]

final

onPanCancel → GestureDragCancelCallback

The pointer that previously triggered onPanDown did not complete. \[...\]

final

onPanDown → void Function(DragDownDetails details)

A pointer has contacted the screen with a primary button and might begin to move. \[...\]

final

onPanEnd → void Function(DragEndDetails details)

A pointer that was previously in contact with the screen with a primary button and moving is no longer in contact with the screen and was moving at a specific velocity when it stopped contacting the screen. \[...\]

final

onPanStart → void Function(DragStartDetails details)

A pointer has contacted the screen with a primary button and has begun to move. \[...\]

final

onPanUpdate → void Function(DragUpdateDetails details)

A pointer that is in contact with the screen with a primary button and moving has moved again. \[...\]

final

onScaleEnd → void Function(ScaleEndDetails details)

The pointers are no longer in contact with the screen.

final

onScaleStart → void Function(ScaleStartDetails details)

The pointers in contact with the screen have established a focal point and initial scale of 1.0.

final

onScaleUpdate → void Function(ScaleUpdateDetails details)

The pointers in contact with the screen have indicated a new focal point and/or scale.

final

onSecondaryLongPress → GestureLongPressCallback

Called when a long press gesture with a secondary button has been recognized. \[...\]

final

onSecondaryLongPressEnd → void Function(LongPressEndDetails details)

A pointer that has triggered a long-press with a secondary button has stopped contacting the screen. \[...\]

final

onSecondaryLongPressMoveUpdate → void Function(LongPressMoveUpdateDetails details)

A pointer has been drag-moved after a long press with a secondary button. \[...\]

final

onSecondaryLongPressStart → void Function(LongPressStartDetails details)

Called when a long press gesture with a secondary button has been recognized. \[...\]

final

onSecondaryLongPressUp → GestureLongPressUpCallback

A pointer that has triggered a long-press with a secondary button has stopped contacting the screen. \[...\]

final

onSecondaryTap → GestureTapCallback

A tap with a secondary button has occurred. \[...\]

final

onSecondaryTapCancel → GestureTapCancelCallback

The pointer that previously triggered onSecondaryTapDown will not end up causing a tap. \[...\]

final

onSecondaryTapDown → void Function(TapDownDetails details)

A pointer that might cause a tap with a secondary button has contacted the screen at a particular location. \[...\]

final

onSecondaryTapUp → void Function(TapUpDetails details)

A pointer that will trigger a tap with a secondary button has stopped contacting the screen at a particular location. \[...\]

final

onTap → GestureTapCallback

A tap with a primary button has occurred. \[...\]

final

onTapCancel → GestureTapCancelCallback

The pointer that previously triggered onTapDown will not end up causing a tap. \[...\]

final

onTapDown → void Function(TapDownDetails details)

A pointer that might cause a tap with a primary button has contacted the screen at a particular location. \[...\]

final

onTapUp → void Function(TapUpDetails details)

A pointer that will trigger a tap with a primary button has stopped contacting the screen at a particular location. \[...\]

final

onTertiaryTapCancel → GestureTapCancelCallback

The pointer that previously triggered onTertiaryTapDown will not end up causing a tap. \[...\]

final

onTertiaryTapDown → void Function(TapDownDetails details)

A pointer that might cause a tap with a tertiary button has contacted the screen at a particular location. \[...\]

final

onTertiaryTapUp → void Function(TapUpDetails details)

A pointer that will trigger a tap with a tertiary button has stopped contacting the screen at a particular location. \[...\]

final

onVerticalDragCancel → GestureDragCancelCallback

The pointer that previously triggered onVerticalDragDown did not complete. \[...\]

final

onVerticalDragDown → void Function(DragDownDetails details)

A pointer has contacted the screen with a primary button and might begin to move vertically. \[...\]

final

onVerticalDragEnd → void Function(DragEndDetails details)

A pointer that was previously in contact with the screen with a primary button and moving vertically is no longer in contact with the screen and was moving at a specific velocity when it stopped contacting the screen. \[...\]

final

onVerticalDragStart → void Function(DragStartDetails details)

A pointer has contacted the screen with a primary button and has begun to move vertically. \[...\]

final

onVerticalDragUpdate → void Function(DragUpdateDetails details)

A pointer that is in contact with the screen with a primary button and moving vertically has moved in the vertical direction. \[...\]

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/gesture_detector.dart#L206
[flutter.dev_gestures]: http://flutter.dev/gestures/