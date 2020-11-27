[*description*][description]

# Padding class #

A widget that insets its child by the given padding.

When passing layout constraints to its child, padding shrinks the constraints by the given padding, causing the child to layout at a smaller size. Padding then sizes itself to its child's size, inflated by the padding, effectively creating empty space around the child.

 *link* 

Sample

This snippet creates "Hello World!" Text inside a Card that is indented by sixteen pixels in each direction.

![padding.png][]

*assignment*

    const Card(
      child: Padding(
        padding: EdgeInsets.all(16.0),
        child: Text('Hello World!'),
      ),
    )

## Design discussion ##

### Why use a Padding widget rather than a Container with a Container.padding property? ###

There isn't really any difference between the two. If you supply a Container.padding argument, Container simply builds a Padding widget for you.

Container doesn't implement its properties directly. Instead, Container combines a number of simpler widgets together into a convenient package. For example, the Container.padding property causes the container to build a Padding widget and the Container.decoration property causes the container to build a DecoratedBox widget. If you find Container convenient, feel free to use it. If not, feel free to build these simpler widgets in whatever combination meets your needs.

In fact, the majority of widgets in Flutter are simply combinations of other simpler widgets. Composition, rather than inheritance, is the primary mechanism for building up widgets.

See also:

 *  AnimatedPadding, which animates changes in padding over a given duration.
 *  EdgeInsets, the class that is used to describe the padding dimensions.
 *  The [catalog of layout widgets][].

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  RenderObjectWidget
 *  SingleChildRenderObjectWidget
 *  Padding

## Constructors ##

Padding(\{Key key, @required EdgeInsetsGeometry padding, Widget child\})

Creates a widget that insets its child. \[...\]

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

padding → EdgeInsetsGeometry

The amount of space by which to inset the child.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

createElement() → SingleChildRenderObjectElement

RenderObjectWidgets always inflate to a RenderObjectElement subclass.

inherited

createRenderObject(BuildContext context) → RenderPadding

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

updateRenderObject(BuildContext context, covariant RenderPadding renderObject) → void

Copies the configuration described by this RenderObjectWidget to the given RenderObject, which will be of the same type as returned by this object's createRenderObject. \[...\]

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

@nonVirtual, inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/basic.dart#L1636
[padding.png]: https://flutter.github.io/assets-for-api-docs/assets/widgets/padding.png
[catalog of layout widgets]: https://flutter.dev/widgets/layout/