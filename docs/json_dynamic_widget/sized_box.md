[*description*][description]

# SizedBox class #

A box with a specified size.

If given a child, this widget forces its child to have a specific width and/or height (assuming values are permitted by this widget's parent). If either the width or height is null, this widget will try to size itself to match the child's size in that dimension. If the child's size depends on the size of its parent, the height and width must be provided.

If not given a child, SizedBox will try to size itself as close to the specified height and width as possible given the parent's constraints. If height or width is null or unspecified, it will be treated as zero.

The new SizedBox.expand constructor can be used to make a SizedBox that sizes itself to fit the parent. It is equivalent to setting width and height to double.infinity.

 *link* 

Sample

This snippet makes the child widget (a Card with some Text) have the exact size 200x300, parental constraints permitting:

*assignment*

    SizedBox(
      width: 200.0,
      height: 300.0,
      child: const Card(child: Text('Hello World!')),
    )

See also:

 *  ConstrainedBox, a more generic version of this class that takes arbitrary BoxConstraints instead of an explicit width and height.
 *  UnconstrainedBox, a container that tries to let its child draw without constraints.
 *  FractionallySizedBox, a widget that sizes its child to a fraction of the total available space.
 *  AspectRatio, a widget that attempts to fit within the parent's constraints while also sizing its child to match a given aspect ratio.
 *  FittedBox, which sizes and positions its child widget to fit the parent according to a given BoxFit discipline.
 *  The [catalog of layout widgets][].

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  RenderObjectWidget
 *  SingleChildRenderObjectWidget
 *  SizedBox

## Constructors ##

SizedBox(\{Key key, double width, double height, Widget child\})

Creates a fixed size box. The `width` and `height` parameters can be null to indicate that the size of the box should not be constrained in the corresponding dimension.

const

SizedBox.expand(\{Key key, Widget child\})

Creates a box that will become as large as its parent allows.

const

SizedBox.fromSize(\{Key key, Widget child, Size size\})

Creates a box with the specified size.

SizedBox.shrink(\{Key key, Widget child\})

Creates a box that will become as small as its parent allows.

const

## Properties ##

child → Widget

The widget below this widget in the tree. \[...\]

final, inherited

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

height → double

If non-null, requires the child to have exactly this height.

final

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

width → double

If non-null, requires the child to have exactly this width.

final

## Methods ##

createElement() → SingleChildRenderObjectElement

RenderObjectWidgets always inflate to a RenderObjectElement subclass.

inherited

createRenderObject(BuildContext context) → RenderConstrainedBox

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

override

updateRenderObject(BuildContext context, covariant RenderConstrainedBox renderObject) → void

Copies the configuration described by this RenderObjectWidget to the given RenderObject, which will be of the same type as returned by this object's createRenderObject. \[...\]

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

@nonVirtual, inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/basic.dart#L2079
[catalog of layout widgets]: https://flutter.dev/widgets/layout/