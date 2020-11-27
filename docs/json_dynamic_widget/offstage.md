[*description*][description]

# Offstage class #

A widget that lays the child out as if it was in the tree, but without painting anything, without making the child available for hit testing, and without taking any room in the parent.

Offstage children are still active: they can receive focus and have keyboard input directed to them.

Animations continue to run in offstage children, and therefore use battery and CPU time, regardless of whether the animations end up being visible.

Offstage can be used to measure the dimensions of a widget without bringing it on screen (yet). To hide a widget from view while it is not needed, prefer removing the widget from the tree entirely rather than keeping it alive in an Offstage subtree.

See also:

 *  Visibility, which can hide a child more efficiently (albeit less subtly).
 *  TickerMode, which can be used to disable animations in a subtree.
 *  The [catalog of layout widgets][].

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  RenderObjectWidget
 *  SingleChildRenderObjectWidget
 *  Offstage

## Constructors ##

Offstage(\{Key key, bool offstage: true, Widget child\})

Creates a widget that visually hides its child.

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

offstage → bool

Whether the child is hidden from the rest of the tree. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

createElement() → \_OffstageElement

RenderObjectWidgets always inflate to a RenderObjectElement subclass.

override

createRenderObject(BuildContext context) → RenderOffstage

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

updateRenderObject(BuildContext context, covariant RenderOffstage renderObject) → void

Copies the configuration described by this RenderObjectWidget to the given RenderObject, which will be of the same type as returned by this object's createRenderObject. \[...\]

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

@nonVirtual, inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/basic.dart#L2673
[catalog of layout widgets]: https://flutter.dev/widgets/layout/