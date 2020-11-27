[*description*][description]

# IndexedStack class #

A Stack that shows a single child from a list of children.

The displayed child is the one with the given index. The stack is always as big as the largest child.

If value is null, then nothing is displayed.

See also:

 *  Stack, for more details about stacks.
 *  The [catalog of layout widgets][].

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  RenderObjectWidget
 *  MultiChildRenderObjectWidget
 *  Stack
 *  IndexedStack

## Constructors ##

IndexedStack(\{Key key, AlignmentGeometry alignment: AlignmentDirectional.topStart, TextDirection textDirection, StackFit sizing: StackFit.loose, int index: 0, List<Widget> children: const <Widget>\[\]\})

Creates a Stack widget that paints a single child. \[...\]

## Properties ##

alignment → AlignmentGeometry

How to align the non-positioned and partially-positioned children in the stack. \[...\]

final, inherited

children → List<Widget>

The widgets below this widget in the tree. \[...\]

final, inherited

clipBehavior → Clip

The content will be clipped (or not) according to this option. \[...\]

final, inherited

fit → StackFit

How to size the non-positioned children in the stack. \[...\]

final, inherited

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

index → int

The index of the child to show.

final

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

overflow → Overflow

Whether overflowing children should be clipped. See Overflow. \[...\]

final, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

textDirection → TextDirection

The text direction with which to resolve alignment. \[...\]

final, inherited

## Methods ##

createElement() → MultiChildRenderObjectElement

RenderObjectWidgets always inflate to a RenderObjectElement subclass.

inherited

createRenderObject(BuildContext context) → RenderIndexedStack

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

updateRenderObject(BuildContext context, covariant RenderIndexedStack renderObject) → void

Copies the configuration described by this RenderObjectWidget to the given RenderObject, which will be of the same type as returned by this object's createRenderObject. \[...\]

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

@nonVirtual, inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/basic.dart#L3394
[catalog of layout widgets]: https://flutter.dev/widgets/layout/