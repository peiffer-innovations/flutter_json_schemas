[*description*][description]

# InteractiveViewer class #

A widget that enables pan and zoom interactions with its child.

The user can transform the child by dragging to pan or pinching to zoom.

By default, InteractiveViewer may draw outside of its original area of the screen, such as when a child is zoomed in and increases in size. However, it will not receive gestures outside of its original area. To prevent InteractiveViewer from drawing outside of its original size, wrap it in a ClipRect. Or, to prevent dead areas where InteractiveViewer does not receive gestures, be sure that the InteractiveViewer widget is the size of the area that should be interactive. See [flutter-go][] for an example of robust positioning of an InteractiveViewer child that works for all screen sizes and child sizes.

The child must not be null.

See also:

 *  The [Flutter Gallery's transformations demo][Flutter Gallery_s transformations demo], which includes the use of InteractiveViewer.

 *link* 

Interactive App Sample code

This example shows a simple Container that can be panned and zoomed.

To create a local project with this code sample, run:  
flutter create --sample=widgets.InteractiveViewer.1 mysample

This example shows a simple Container that can be panned and zoomed.

*assignment*

    Widget build(BuildContext context) {
      return Center(
        child: InteractiveViewer(
          boundaryMargin: EdgeInsets.all(20.0),
          minScale: 0.1,
          maxScale: 1.6,
          child: Container(
            decoration: BoxDecoration(
              gradient: LinearGradient(
                begin: Alignment.topCenter,
                end: Alignment.bottomCenter,
                colors: <Color>[Colors.orange, Colors.red],
                stops: <double>[0.0, 1.0],
              ),
            ),
          ),
        ),
      );
    }

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatefulWidget
 *  InteractiveViewer

Annotations

 *  @immutable

## Constructors ##

InteractiveViewer(\{Key key, bool alignPanAxis: false, EdgeInsets boundaryMargin: EdgeInsets.zero, bool constrained: true, double maxScale: 2.5, double minScale: 0.8, void onInteractionEnd(ScaleEndDetails details), void onInteractionStart(ScaleStartDetails details), void onInteractionUpdate(ScaleUpdateDetails details), bool panEnabled: true, bool scaleEnabled: true, TransformationController transformationController, @required Widget child\})

Create an InteractiveViewer. \[...\]

## Properties ##

alignPanAxis → bool

If true, panning is only allowed in the direction of the horizontal axis or the vertical axis. \[...\]

final

boundaryMargin → EdgeInsets

A margin for the visible boundaries of the child. \[...\]

final

child → Widget

The Widget to perform the transformations on. \[...\]

final

constrained → bool

Whether the normal size constraints at this point in the widget tree are applied to the child. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

maxScale → double

The maximum allowed scale. \[...\]

final

minScale → double

The minimum allowed scale. \[...\]

final

onInteractionEnd → void Function(ScaleEndDetails details)

Called when the user ends a pan or scale gesture on the widget. \[...\]

final

onInteractionStart → void Function(ScaleStartDetails details)

Called when the user begins a pan or scale gesture on the widget. \[...\]

final

onInteractionUpdate → void Function(ScaleUpdateDetails details)

Called when the user updates a pan or scale gesture on the widget. \[...\]

final

panEnabled → bool

If false, the user will be prevented from panning. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

scaleEnabled → bool

If false, the user will be prevented from scaling. \[...\]

final

transformationController → TransformationController

A TransformationController for the transformation performed on the child. \[...\]

final

## Methods ##

createElement() → StatefulElement

Creates a StatefulElement to manage this widget's location in the tree. \[...\]

inherited

createState() → \_InteractiveViewerState

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

## Static Methods ##

getAxisAlignedBoundingBox(Quad quad) → Quad

Given a quad, return its axis aligned bounding box.

@visibleForTesting

getNearestPointInside(Vector3 point, Quad quad) → Vector3

Get the point inside (inclusively) the given Quad that is nearest to the given Vector3.

@visibleForTesting

getNearestPointOnLine(Vector3 point, Vector3 l1, Vector3 l2) → Vector3

Returns the closest point to the given point on the given line segment.

@visibleForTesting

pointIsInside(Vector3 point, Quad quad) → bool

Returns true iff the point is inside the rectangle given by the Quad, inclusively. Algorithm from [https://math.stackexchange.com/a/190373][https_math.stackexchange.com_a_190373].

@visibleForTesting


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/interactive_viewer.dart#L65
[flutter-go]: https://github.com/justinmc/flutter-go
[Flutter Gallery_s transformations demo]: https://github.com/flutter/gallery/blob/master/lib/demos/reference/transformations_demo.dart
[https_math.stackexchange.com_a_190373]: https://math.stackexchange.com/a/190373