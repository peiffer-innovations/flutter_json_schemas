[*description*][description]

# OverflowBox class #

A widget that imposes different constraints on its child than it gets from its parent, possibly allowing the child to overflow the parent.

See also:

 *  RenderConstrainedOverflowBox for details about how OverflowBox is rendered.
 *  SizedOverflowBox, a widget that is a specific size but passes its original constraints through to its child, which may then overflow.
 *  ConstrainedBox, a widget that imposes additional constraints on its child.
 *  UnconstrainedBox, a container that tries to let its child draw without constraints.
 *  SizedBox, a box with a specified size.
 *  The [catalog of layout widgets][].

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  RenderObjectWidget
 *  SingleChildRenderObjectWidget
 *  OverflowBox

## Constructors ##

OverflowBox(\{Key key, AlignmentGeometry alignment: Alignment.center, double minWidth, double maxWidth, double minHeight, double maxHeight, Widget child\})

Creates a widget that lets its child overflow itself.

const

## Properties ##

alignment → AlignmentGeometry

How to align the child. \[...\]

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

maxHeight → double

The maximum height constraint to give the child. Set this to null (the default) to use the constraint from the parent instead.

final

maxWidth → double

The maximum width constraint to give the child. Set this to null (the default) to use the constraint from the parent instead.

final

minHeight → double

The minimum height constraint to give the child. Set this to null (the default) to use the constraint from the parent instead.

final

minWidth → double

The minimum width constraint to give the child. Set this to null (the default) to use the constraint from the parent instead.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

createElement() → SingleChildRenderObjectElement

RenderObjectWidgets always inflate to a RenderObjectElement subclass.

inherited

createRenderObject(BuildContext context) → RenderConstrainedOverflowBox

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

updateRenderObject(BuildContext context, covariant RenderConstrainedOverflowBox renderObject) → void

Copies the configuration described by this RenderObjectWidget to the given RenderObject, which will be of the same type as returned by this object's createRenderObject. \[...\]

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

@nonVirtual, inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/basic.dart#L2496
[catalog of layout widgets]: https://flutter.dev/widgets/layout/