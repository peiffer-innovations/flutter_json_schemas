[*description*][description]

# AnimatedPositioned class #

Animated version of Positioned which automatically transitions the child's position over a given duration whenever the given position changes.

Only works if it's the child of a Stack.

This widget is a good choice if the *size* of the child would end up changing as a result of this animation. If the size is intended to remain the same, with only the *position* changing over time, then consider SlideTransition instead. SlideTransition only triggers a repaint each frame of the animation, whereas AnimatedPositioned will trigger a relayout as well.

Here's an illustration of what using this widget looks like, using a curve of Curves.fastOutSlowIn.

For the animation, you can choose a curve as well as a duration and the widget will automatically animate to the new target position. If you require more control over the animation (e.g. if you want to stop it mid-animation), consider using a PositionedTransition instead, which takes a provided Animation as an argument. While that allows you to fine-tune the animation, it also requires more development overhead as you have to manually manage the lifecycle of the underlying AnimationController.

See also:

 *  AnimatedPositionedDirectional, which adapts to the ambient Directionality (the same as this widget, but for animating PositionedDirectional).

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatefulWidget
 *  ImplicitlyAnimatedWidget
 *  AnimatedPositioned

## Constructors ##

AnimatedPositioned(\{Key key, @required Widget child, double left, double top, double right, double bottom, double width, double height, Curve curve: Curves.linear, @required Duration duration, VoidCallback onEnd\})

Creates a widget that animates its position implicitly. \[...\]

const

AnimatedPositioned.fromRect(\{Key key, Widget child, Rect rect, Curve curve: Curves.linear, @required Duration duration, VoidCallback onEnd\})

Creates a widget that animates the rectangle it occupies implicitly. \[...\]

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

The offset of the child's left edge from the left of the stack.

final

onEnd → VoidCallback

Called every time an animation completes. \[...\]

final, inherited

right → double

The offset of the child's right edge from the right of the stack.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

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

createState() → \_AnimatedPositionedState

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/implicit_animations.dart#L1005