[*description*][description]

# AnimatedPhysicalModel class #

Animated version of PhysicalModel.

The borderRadius and elevation are animated.

The color is animated if the animateColor property is set; otherwise, the color changes immediately at the start of the animation for the other two properties. This allows the color to be animated independently (e.g. because it is being driven by an AnimatedTheme).

The shape is not animated.

Here's an illustration of what using this widget looks like, using a curve of Curves.fastOutSlowIn.

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatefulWidget
 *  ImplicitlyAnimatedWidget
 *  AnimatedPhysicalModel

## Constructors ##

AnimatedPhysicalModel(\{Key key, @required Widget child, @required BoxShape shape, Clip clipBehavior: Clip.none, BorderRadius borderRadius: BorderRadius.zero, @required double elevation, @required Color color, bool animateColor: true, @required Color shadowColor, bool animateShadowColor: true, Curve curve: Curves.linear, @required Duration duration, VoidCallback onEnd\})

Creates a widget that animates the properties of a PhysicalModel. \[...\]

const

## Properties ##

animateColor → bool

Whether the color should be animated.

final

animateShadowColor → bool

Whether the shadow color should be animated.

final

borderRadius → BorderRadius

The target border radius of the rounded corners for a rectangle shape.

final

child → Widget

The widget below this widget in the tree. \[...\]

final

clipBehavior → Clip

The content will be clipped (or not) according to this option. \[...\]

final

color → Color

The target background color.

final

curve → Curve

The curve to apply when animating the parameters of this container.

final, inherited

duration → Duration

The duration over which to animate the parameters of this container.

final, inherited

elevation → double

The target z-coordinate relative to the parent at which to place this physical object. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

onEnd → VoidCallback

Called every time an animation completes. \[...\]

final, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

shadowColor → Color

The target shadow color.

final

shape → BoxShape

The type of shape. \[...\]

final

## Methods ##

createElement() → StatefulElement

Creates a StatefulElement to manage this widget's location in the tree. \[...\]

inherited

createState() → \_AnimatedPhysicalModelState

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/implicit_animations.dart#L1677