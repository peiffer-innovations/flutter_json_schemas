[*description*][description]

# AnimatedDefaultTextStyle class #

Animated version of DefaultTextStyle which automatically transitions the default text style (the text style to apply to descendant Text widgets without explicit style) over a given duration whenever the given style changes.

The textAlign, softWrap, overflow, maxLines, textWidthBasis and textHeightBehavior properties are not animated and take effect immediately when changed.

Here's an illustration of what using this widget looks like, using a curve of Curves.elasticInOut.

For the animation, you can choose a curve as well as a duration and the widget will automatically animate to the new default text style. If you require more control over the animation (e.g. if you want to stop it mid-animation), consider using a DefaultTextStyleTransition instead, which takes a provided Animation as argument. While that allows you to fine-tune the animation, it also requires more development overhead as you have to manually manage the lifecycle of the underlying AnimationController.

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatefulWidget
 *  ImplicitlyAnimatedWidget
 *  AnimatedDefaultTextStyle

## Constructors ##

AnimatedDefaultTextStyle(\{Key key, @required Widget child, @required TextStyle style, TextAlign textAlign, bool softWrap: true, TextOverflow overflow: TextOverflow.clip, int maxLines, TextWidthBasis textWidthBasis: TextWidthBasis.parent, TextHeightBehavior textHeightBehavior, Curve curve: Curves.linear, @required Duration duration, VoidCallback onEnd\})

Creates a widget that animates the default text style implicitly. \[...\]

const

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

maxLines → int

An optional maximum number of lines for the text to span, wrapping if necessary. \[...\]

final

onEnd → VoidCallback

Called every time an animation completes. \[...\]

final, inherited

overflow → TextOverflow

How visual overflow should be handled. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

softWrap → bool

Whether the text should break at soft line breaks. \[...\]

final

style → TextStyle

The target text style. \[...\]

final

textAlign → TextAlign

How the text should be aligned horizontally. \[...\]

final

textHeightBehavior → TextHeightBehavior

Defines how the paragraph will apply TextStyle.height to the ascent of the first line and descent of the last line. \[...\]

final

textWidthBasis → TextWidthBasis

The strategy to use when calculating the width of the Text. \[...\]

final

## Methods ##

createElement() → StatefulElement

Creates a StatefulElement to manage this widget's location in the tree. \[...\]

inherited

createState() → \_AnimatedDefaultTextStyleState

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/implicit_animations.dart#L1554