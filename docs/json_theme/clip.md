[*description*][description]

# ClipRect class #

A widget that clips its child using a rectangle.

By default, ClipRect prevents its child from painting outside its bounds, but the size and location of the clip rect can be customized using a custom clipper.

ClipRect is commonly used with these widgets, which commonly paint outside their bounds:

 *  CustomPaint
 *  CustomSingleChildLayout
 *  CustomMultiChildLayout
 *  Align and Center (e.g., if Align.widthFactor or Align.heightFactor is less than 1.0).
 *  OverflowBox
 *  SizedOverflowBox

 *link* 

Sample

For example, by combining a ClipRect with an Align, one can show just the top half of an Image:

*assignment*

    ClipRect(
      child: Align(
        alignment: Alignment.topCenter,
        heightFactor: 0.5,
        child: Image.network(userAvatarUrl),
      ),
    )

See also:

 *  CustomClipper, for information about creating custom clips.
 *  ClipRRect, for a clip with rounded corners.
 *  ClipOval, for an elliptical clip.
 *  ClipPath, for an arbitrarily shaped clip.

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  RenderObjectWidget
 *  SingleChildRenderObjectWidget
 *  ClipRect

## Constructors ##

ClipRect(\{Key key, CustomClipper<Rect> clipper, Clip clipBehavior: Clip.hardEdge, Widget child\})

Creates a rectangular clip. \[...\]

const

## Properties ##

child → Widget

The widget below this widget in the tree. \[...\]

final, inherited

clipBehavior → Clip

Controls how to clip. \[...\]

final

clipper → CustomClipper<Rect>

If non-null, determines which clip to use.

final

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

createRenderObject(BuildContext context) → RenderClipRect

Creates an instance of the RenderObject class that this RenderObjectWidget represents, using the configuration described by this RenderObjectWidget. \[...\]

override

debugDescribeChildren() → List<DiagnosticsNode>

Returns a list of DiagnosticsNode objects describing this node's children. \[...\]

@protected, inherited

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

override

didUnmountRenderObject(covariant RenderClipRect renderObject) → void

A render object previously associated with this widget has been removed from the tree. The given RenderObject will be of the same type as returned by this object's createRenderObject.

override

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

updateRenderObject(BuildContext context, covariant RenderClipRect renderObject) → void

Copies the configuration described by this RenderObjectWidget to the given RenderObject, which will be of the same type as returned by this object's createRenderObject. \[...\]

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

@nonVirtual, inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/basic.dart#L592