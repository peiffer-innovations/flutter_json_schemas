[*description*][description]

# AnimatedAlign class #

Animated version of Align which automatically transitions the child's position over a given duration whenever the given alignment changes.

Here's an illustration of what this can look like, using a curve of Curves.fastOutSlowIn.

For the animation, you can choose a curve as well as a duration and the widget will automatically animate to the new target alignment. If you require more control over the animation (e.g. if you want to stop it mid-animation), consider using an AlignTransition instead, which takes a provided Animation as argument. While that allows you to fine-tune the animation, it also requires more development overhead as you have to manually manage the lifecycle of the underlying AnimationController.

See also:

 *  AnimatedContainer, which can transition more values at once.
 *  AnimatedPadding, which can animate the padding instead of the alignment.
 *  AnimatedPositioned, which, as a child of a Stack, automatically transitions its child's position over a given duration whenever the given position changes.

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatefulWidget
 *  ImplicitlyAnimatedWidget
 *  AnimatedAlign

## Constructors ##

AnimatedAlign(\{Key key, @required AlignmentGeometry alignment, Widget child, double heightFactor, double widthFactor, Curve curve: Curves.linear, @required Duration duration, VoidCallback onEnd\})

Creates a widget that positions its child by an alignment that animates implicitly. \[...\]

const

## Properties ##

alignment → AlignmentGeometry

How to align the child. \[...\]

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

heightFactor → double

If non-null, sets its height to the child's height multiplied by this factor. \[...\]

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

widthFactor → double

If non-null, sets its width to the child's width multiplied by this factor. \[...\]

final

## Methods ##

createElement() → StatefulElement

Creates a StatefulElement to manage this widget's location in the tree. \[...\]

inherited

createState() → \_AnimatedAlignState

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/implicit_animations.dart#L877