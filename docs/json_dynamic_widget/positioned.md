[*description*][description]

# Positioned class #

A widget that controls where a child of a Stack is positioned.

A Positioned widget must be a descendant of a Stack, and the path from the Positioned widget to its enclosing Stack must contain only StatelessWidgets or StatefulWidgets (not other kinds of widgets, like RenderObjectWidgets).

If a widget is wrapped in a Positioned, then it is a *positioned* widget in its Stack. If the top property is non-null, the top edge of this child will be positioned top layout units from the top of the stack widget. The right, bottom, and left properties work analogously.

If both the top and bottom properties are non-null, then the child will be forced to have exactly the height required to satisfy both constraints. Similarly, setting the right and left properties to non-null values will force the child to have a particular width. Alternatively the width and height properties can be used to give the dimensions, with one corresponding position property (e.g. top and height).

If all three values on a particular axis are null, then the Stack.alignment property is used to position the child.

If all six values are null, the child is a non-positioned child. The Stack uses only the non-positioned children to size itself.

See also:

 *  AnimatedPositioned, which automatically transitions the child's position over a given duration whenever the given position changes.
 *  PositionedTransition, which takes a provided Animation to transition changes in the child's position over a given duration.
 *  PositionedDirectional, which adapts to the ambient Directionality.

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  ProxyWidget
 *  ParentDataWidget<StackParentData>
 *  Positioned

## Constructors ##

Positioned(\{Key key, double left, double top, double right, double bottom, double width, double height, @required Widget child\})

Creates a widget that controls where a child of a Stack is positioned. \[...\]

const

Positioned.directional(\{Key key, @required TextDirection textDirection, double start, double top, double end, double bottom, double width, double height, @required Widget child\})

Creates a widget that controls where a child of a Stack is positioned. \[...\]

factory

Positioned.fill(\{Key key, double left: 0.0, double top: 0.0, double right: 0.0, double bottom: 0.0, @required Widget child\})

Creates a Positioned object with `left`, `top`, `right`, and `bottom` set to 0.0 unless a value for them is passed.

const

Positioned.fromRect(\{Key key, Rect rect, @required Widget child\})

Creates a Positioned object with the values from the given Rect. \[...\]

Positioned.fromRelativeRect(\{Key key, RelativeRect rect, @required Widget child\})

Creates a Positioned object with the values from the given RelativeRect. \[...\]

## Properties ##

bottom → double

The distance that the child's bottom edge is inset from the bottom of the stack. \[...\]

final

child → Widget

The widget below this widget in the tree. \[...\]

final, inherited

debugTypicalAncestorWidgetClass → Type

The RenderObjectWidget that is typically used to set up the ParentData that applyParentData will write to. \[...\]

read-only, override

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

height → double

The child's height. \[...\]

final

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

left → double

The distance that the child's left edge is inset from the left of the stack. \[...\]

final

right → double

The distance that the child's right edge is inset from the right of the stack. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

top → double

The distance that the child's top edge is inset from the top of the stack. \[...\]

final

width → double

The child's width. \[...\]

final

## Methods ##

applyParentData(RenderObject renderObject) → void

Write the data from this widget into the given render object's parent data. \[...\]

override

createElement() → ParentDataElement<StackParentData>

Inflates this configuration to a concrete instance. \[...\]

inherited

debugCanApplyOutOfTurn() → bool

Whether the ParentDataElement.applyWidgetOutOfTurn method is allowed with this widget. \[...\]

@protected, inherited

debugDescribeChildren() → List<DiagnosticsNode>

Returns a list of DiagnosticsNode objects describing this node's children. \[...\]

@protected, inherited

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

override

debugIsValidRenderObject(RenderObject renderObject) → bool

Checks if this widget can apply its parent data to the provided `renderObject`. \[...\]

inherited

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

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

@nonVirtual, inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/basic.dart#L3464