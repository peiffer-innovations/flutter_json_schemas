[*description*][description]

# AnimatedPositionedDirectional class #

Animated version of PositionedDirectional which automatically transitions the child's position over a given duration whenever the given position changes.

The ambient Directionality is used to determine whether start is to the left or to the right.

Only works if it's the child of a Stack.

This widget is a good choice if the *size* of the child would end up changing as a result of this animation. If the size is intended to remain the same, with only the *position* changing over time, then consider SlideTransition instead. SlideTransition only triggers a repaint each frame of the animation, whereas AnimatedPositionedDirectional will trigger a relayout as well. (SlideTransition is also text-direction-aware.)

Here's an illustration of what using this widget looks like, using a curve of Curves.fastOutSlowIn.

See also:

 *  AnimatedPositioned, which specifies the widget's position visually (the same as this widget, but for animating Positioned).

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatefulWidget
 *  ImplicitlyAnimatedWidget
 *  AnimatedPositionedDirectional

## Constructors ##

AnimatedPositionedDirectional(\{Key key, @required Widget child, double start, double top, double end, double bottom, double width, double height, Curve curve: Curves.linear, @required Duration duration, VoidCallback onEnd\})

Creates a widget that animates its position implicitly. \[...\]

const

## Properties ##

bottom → double

The offset of the child's bottom edge from the bottom of the stack.

final

child → Widget

The widget below this widget in the tree. \[...\]

final

curve → Curve

The curve to apply when animating the parameters of this container.

final, inherited

duration → Duration

The duration over which to animate the parameters of this container.

final, inherited

end → double

The offset of the child's end edge from the end of the stack.

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

height → double

The child's height. \[...\]

final

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

onEnd → VoidCallback

Called every time an animation completes. \[...\]

final, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

start → double

The offset of the child's start edge from the start of the stack.

final

top → double

The offset of the child's top edge from the top of the stack.

final

width → double

The child's width. \[...\]

final

## Methods ##

createElement() → StatefulElement

Creates a StatefulElement to manage this widget's location in the tree. \[...\]

inherited

createState() → \_AnimatedPositionedDirectionalState

Creates the mutable state for this widget at a given location in the tree. \[...\]

override

debugDescribeChildren() → List<DiagnosticsNode>

Returns a list of DiagnosticsNode objects describing this node's children. \[...\]

@protected, inherited

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

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

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

@nonVirtual, inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/implicit_animations.dart#L1159