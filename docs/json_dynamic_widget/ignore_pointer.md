[*description*][description]

# IgnorePointer class #

A widget that is invisible during hit testing.

When ignoring is true, this widget (and its subtree) is invisible to hit testing. It still consumes space during layout and paints its child as usual. It just cannot be the target of located events, because it returns false from RenderBox.hitTest.

When ignoringSemantics is true, the subtree will be invisible to the semantics layer (and thus e.g. accessibility tools). If ignoringSemantics is null, it uses the value of ignoring.

See also:

 *  AbsorbPointer, which also prevents its children from receiving pointer events but is itself visible to hit testing.

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  RenderObjectWidget
 *  SingleChildRenderObjectWidget
 *  IgnorePointer

## Constructors ##

IgnorePointer(\{Key key, bool ignoring: true, bool ignoringSemantics, Widget child\})

Creates a widget that is invisible to hit testing. \[...\]

const

## Properties ##

child → Widget

The widget below this widget in the tree. \[...\]

final, inherited

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

ignoring → bool

Whether this widget is ignored during hit testing. \[...\]

final

ignoringSemantics → bool

Whether the semantics of this widget is ignored when compiling the semantics tree. \[...\]

final

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

createRenderObject(BuildContext context) → RenderIgnorePointer

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

updateRenderObject(BuildContext context, covariant RenderIgnorePointer renderObject) → void

Copies the configuration described by this RenderObjectWidget to the given RenderObject, which will be of the same type as returned by this object's createRenderObject. \[...\]

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

@nonVirtual, inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/basic.dart#L6450