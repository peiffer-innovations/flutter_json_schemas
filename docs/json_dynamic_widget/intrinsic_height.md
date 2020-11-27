[*description*][description]

# IntrinsicHeight class #

A widget that sizes its child to the child's intrinsic height.

This class is useful, for example, when unlimited height is available and you would like a child that would otherwise attempt to expand infinitely to instead size itself to a more reasonable height.

The constraints that this widget passes to its child will adhere to the parent's constraints, so if the constraints are not large enough to satisfy the child's maximum intrinsic height, then the child will get less height than it otherwise would. Likewise, if the minimum height constraint is larger than the child's maximum intrinsic height, the child will be given more height than it otherwise would.

This class is relatively expensive, because it adds a speculative layout pass before the final layout phase. Avoid using it where possible. In the worst case, this widget can result in a layout that is O(N²) in the depth of the tree.

See also:

 *  Align, a widget that aligns its child within itself. This can be used to loosen the constraints passed to the RenderIntrinsicHeight, allowing the RenderIntrinsicHeight's child to be smaller than that of its parent.
 *  Column, which when used with CrossAxisAlignment.stretch can be used to loosen just the height constraints that are passed to the RenderIntrinsicHeight, allowing the RenderIntrinsicHeight's child's height to be smaller than that of its parent.
 *  [The catalog of layout widgets][].

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  RenderObjectWidget
 *  SingleChildRenderObjectWidget
 *  IntrinsicHeight

## Constructors ##

IntrinsicHeight(\{Key key, Widget child\})

Creates a widget that sizes its child to the child's intrinsic height. \[...\]

const

## Properties ##

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

createRenderObject(BuildContext context) → RenderIntrinsicHeight

Creates an instance of the RenderObject class that this RenderObjectWidget represents, using the configuration described by this RenderObjectWidget. \[...\]

override

debugDescribeChildren() → List<DiagnosticsNode>

Returns a list of DiagnosticsNode objects describing this node's children. \[...\]

@protected, inherited

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

inherited

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

updateRenderObject(BuildContext context, covariant RenderObject renderObject) → void

Copies the configuration described by this RenderObjectWidget to the given RenderObject, which will be of the same type as returned by this object's createRenderObject. \[...\]

@protected, inherited

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

@nonVirtual, inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/basic.dart#L2904
[The catalog of layout widgets]: https://flutter.dev/widgets/layout/