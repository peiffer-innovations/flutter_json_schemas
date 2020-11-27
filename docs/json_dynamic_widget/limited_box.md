[*description*][description]

# LimitedBox class #

A box that limits its size only when it's unconstrained.

If this widget's maximum width is unconstrained then its child's width is limited to maxWidth. Similarly, if this widget's maximum height is unconstrained then its child's height is limited to maxHeight.

This has the effect of giving the child a natural dimension in unbounded environments. For example, by providing a maxHeight to a widget that normally tries to be as big as possible, the widget will normally size itself to fit its parent, but when placed in a vertical list, it will take on the given height.

This is useful when composing widgets that normally try to match their parents' size, so that they behave reasonably in lists (which are unbounded).

See also:

 *  ConstrainedBox, which applies its constraints in all cases, not just when the incoming constraints are unbounded.
 *  SizedBox, which lets you specify tight constraints by explicitly specifying the height or width.
 *  The [catalog of layout widgets][].

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  RenderObjectWidget
 *  SingleChildRenderObjectWidget
 *  LimitedBox

## Constructors ##

LimitedBox(\{Key key, double maxWidth: double.infinity, double maxHeight: double.infinity, Widget child\})

Creates a box that limits its size only when it's unconstrained. \[...\]

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

maxHeight → double

The maximum height limit to apply in the absence of a BoxConstraints.maxHeight constraint.

final

maxWidth → double

The maximum width limit to apply in the absence of a BoxConstraints.maxWidth constraint.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

createElement() → SingleChildRenderObjectElement

RenderObjectWidgets always inflate to a RenderObjectElement subclass.

inherited

createRenderObject(BuildContext context) → RenderLimitedBox

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

updateRenderObject(BuildContext context, covariant RenderLimitedBox renderObject) → void

Copies the configuration described by this RenderObjectWidget to the given RenderObject, which will be of the same type as returned by this object's createRenderObject. \[...\]

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

@nonVirtual, inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/basic.dart#L2436
[catalog of layout widgets]: https://flutter.dev/widgets/layout/