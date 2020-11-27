[*description*][description]

# Opacity class #

A widget that makes its child partially transparent.

This class paints its child into an intermediate buffer and then blends the child back into the scene partially transparent.

For values of opacity other than 0.0 and 1.0, this class is relatively expensive because it requires painting the child into an intermediate buffer. For the value 0.0, the child is simply not painted at all. For the value 1.0, the child is painted immediately without an intermediate buffer.

 *link* 

Sample

This example shows some Text when the `_visible` member field is true, and hides it when it is false:

*assignment*

    Opacity(
      opacity: _visible ? 1.0 : 0.0,
      child: const Text("Now you see me, now you don't!"),
    )

This is more efficient than adding and removing the child widget from the tree on demand.

## Performance considerations for opacity animation ##

Animating an Opacity widget directly causes the widget (and possibly its subtree) to rebuild each frame, which is not very efficient. Consider using an AnimatedOpacity instead.

## Transparent image ##

If only a single Image or Color needs to be composited with an opacity between 0.0 and 1.0, it's much faster to directly use them without Opacity widgets.

For example, `Container(color: Color.fromRGBO(255, 0, 0, 0.5))` is much faster than `Opacity(opacity: 0.5, child: Container(color: Colors.red))`.

 *link* 

Sample

The following example draws an Image with 0.5 opacity without using Opacity:

*assignment*

    Image.network(
      'https://raw.githubusercontent.com/flutter/assets-for-api-docs/master/packages/diagrams/assets/blend_mode_destination.jpeg',
      color: Color.fromRGBO(255, 255, 255, 0.5),
      colorBlendMode: BlendMode.modulate
    )

Directly drawing an Image or Color with opacity is faster than using Opacity on top of them because Opacity could apply the opacity to a group of widgets and therefore a costly offscreen buffer will be used. Drawing content into the offscreen buffer may also trigger render target switches and such switching is particularly slow in older GPUs.

See also:

 *  Visibility, which can hide a child more efficiently (albeit less subtly, because it is either visible or hidden, rather than allowing fractional opacity values).
 *  ShaderMask, which can apply more elaborate effects to its child.
 *  Transform, which applies an arbitrary transform to its child widget at paint time.
 *  AnimatedOpacity, which uses an animation internally to efficiently animate opacity.
 *  FadeTransition, which uses a provided animation to efficiently animate opacity.
 *  Image, which can directly provide a partially transparent image with much less performance hit.

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  RenderObjectWidget
 *  SingleChildRenderObjectWidget
 *  Opacity

## Constructors ##

Opacity(\{Key key, @required double opacity, bool alwaysIncludeSemantics: false, Widget child\})

Creates a widget that makes its child partially transparent. \[...\]

const

## Properties ##

alwaysIncludeSemantics → bool

Whether the semantic information of the children is always included. \[...\]

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

opacity → double

The fraction to scale the child's alpha value. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

createElement() → SingleChildRenderObjectElement

RenderObjectWidgets always inflate to a RenderObjectElement subclass.

inherited

createRenderObject(BuildContext context) → RenderOpacity

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

updateRenderObject(BuildContext context, covariant RenderOpacity renderObject) → void

Copies the configuration described by this RenderObjectWidget to the given RenderObject, which will be of the same type as returned by this object's createRenderObject. \[...\]

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

@nonVirtual, inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/basic.dart#L208