[*description*][description]

# AspectRatio class #

A widget that attempts to size the child to a specific aspect ratio.

The widget first tries the largest width permitted by the layout constraints. The height of the widget is determined by applying the given aspect ratio to the width, expressed as a ratio of width to height.

For example, a 16:9 width:height aspect ratio would have a value of 16.0/9.0. If the maximum width is infinite, the initial width is determined by applying the aspect ratio to the maximum height.

Now consider a second example, this time with an aspect ratio of 2.0 and layout constraints that require the width to be between 0.0 and 100.0 and the height to be between 0.0 and 100.0. We'll select a width of 100.0 (the biggest allowed) and a height of 50.0 (to match the aspect ratio).

In that same situation, if the aspect ratio is 0.5, we'll also select a width of 100.0 (still the biggest allowed) and we'll attempt to use a height of 200.0. Unfortunately, that violates the constraints because the child can be at most 100.0 pixels tall. The widget will then take that value and apply the aspect ratio again to obtain a width of 50.0. That width is permitted by the constraints and the child receives a width of 50.0 and a height of 100.0. If the width were not permitted, the widget would continue iterating through the constraints. If the widget does not find a feasible size after consulting each constraint, the widget will eventually select a size for the child that meets the layout constraints but fails to meet the aspect ratio constraints.

See also:

 *  Align, a widget that aligns its child within itself and optionally sizes itself based on the child's size.
 *  ConstrainedBox, a widget that imposes additional constraints on its child.
 *  UnconstrainedBox, a container that tries to let its child draw without constraints.
 *  The [catalog of layout widgets][].

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  RenderObjectWidget
 *  SingleChildRenderObjectWidget
 *  AspectRatio

## Constructors ##

AspectRatio(\{Key key, @required double aspectRatio, Widget child\})

Creates a widget with a specific aspect ratio. \[...\]

const

## Properties ##

aspectRatio → double

The aspect ratio to attempt to use. \[...\]

final

child → Widget

The widget below this widget in the tree. \[...\]

final, inherited

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

createElement() → SingleChildRenderObjectElement

RenderObjectWidgets always inflate to a RenderObjectElement subclass.

inherited

createRenderObject(BuildContext context) → RenderAspectRatio

Creates an instance of the RenderObject class that this RenderObjectWidget represents, using the configuration described by this RenderObjectWidget. \[...\]

override

debugDescribeChildren() → List<DiagnosticsNode>

Returns a list of DiagnosticsNode objects describing this node's children. \[...\]

@protected, inherited

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

override

didUnmountRenderObject(covariant RenderObject renderObject) → void

A render object previously associated with this widget has been removed from the tree. The given RenderObject will be of the same type as returned by this object's createRenderObject.

@protected, inherited

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

updateRenderObject(BuildContext context, covariant RenderAspectRatio renderObject) → void

Copies the configuration described by this RenderObjectWidget to the given RenderObject, which will be of the same type as returned by this object's createRenderObject. \[...\]

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

@nonVirtual, inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/basic.dart#L2763
[catalog of layout widgets]: https://flutter.dev/widgets/layout/