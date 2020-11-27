[*description*][description]

# DecoratedBox class #

A widget that paints a Decoration either before or after its child paints.

Container insets its child by the widths of the borders; this widget does not.

Commonly used with BoxDecoration.

The child is not clipped. To clip a child to the shape of a particular ShapeDecoration, consider using a ClipPath widget.

 *link* 

Sample

This sample shows a radial gradient that draws a moon on a night sky:

*assignment*

    DecoratedBox(
      decoration: BoxDecoration(
        gradient: RadialGradient(
          center: const Alignment(-0.5, -0.6),
          radius: 0.15,
          colors: <Color>[
            const Color(0xFFEEEEEE),
            const Color(0xFF111133),
          ],
          stops: <double>[0.9, 1.0],
        ),
      ),
    )

See also:

 *  Ink, which paints a Decoration on a Material, allowing InkResponse and InkWell splashes to paint over them.
 *  DecoratedBoxTransition, the version of this class that animates on the decoration property.
 *  Decoration, which you can extend to provide other effects with DecoratedBox.
 *  CustomPaint, another way to draw custom effects from the widget layer.

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  RenderObjectWidget
 *  SingleChildRenderObjectWidget
 *  DecoratedBox

## Constructors ##

DecoratedBox(\{Key key, @required Decoration decoration, DecorationPosition position: DecorationPosition.background, Widget child\})

Creates a widget that paints a Decoration. \[...\]

const

## Properties ##

child → Widget

The widget below this widget in the tree. \[...\]

final, inherited

decoration → Decoration

What decoration to paint. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

position → DecorationPosition

Whether to paint the box decoration behind or in front of the child.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

createElement() → SingleChildRenderObjectElement

RenderObjectWidgets always inflate to a RenderObjectElement subclass.

inherited

createRenderObject(BuildContext context) → RenderDecoratedBox

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

updateRenderObject(BuildContext context, covariant RenderDecoratedBox renderObject) → void

Copies the configuration described by this RenderObjectWidget to the given RenderObject, which will be of the same type as returned by this object's createRenderObject. \[...\]

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

@nonVirtual, inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/container.dart#L58