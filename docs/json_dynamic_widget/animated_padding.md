[*description*][description]

# AnimatedPadding class #

Animated version of Padding which automatically transitions the indentation over a given duration whenever the given inset changes.

Here's an illustration of what using this widget looks like, using a curve of Curves.fastOutSlowIn.

See also:

 *  AnimatedContainer, which can transition more values at once.
 *  AnimatedAlign, which automatically transitions its child's position over a given duration whenever the given AnimatedAlign.alignment changes.

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatefulWidget
 *  ImplicitlyAnimatedWidget
 *  AnimatedPadding

## Constructors ##

AnimatedPadding(\{Key key, @required EdgeInsetsGeometry padding, Widget child, Curve curve: Curves.linear, @required Duration duration, VoidCallback onEnd\})

Creates a widget that insets its child by a value that animates implicitly. \[...\]

## Properties ##

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

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

onEnd → VoidCallback

Called every time an animation completes. \[...\]

final, inherited

padding → EdgeInsetsGeometry

The amount of space by which to inset the child.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

createElement() → StatefulElement

Creates a StatefulElement to manage this widget's location in the tree. \[...\]

inherited

createState() → \_AnimatedPaddingState

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/implicit_animations.dart#L795