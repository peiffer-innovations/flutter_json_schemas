[*description*][description]

# AnimatedTheme class #

Animated version of Theme which automatically transitions the colors, etc, over a given duration whenever the given theme changes.

Here's an illustration of what using this widget looks like, using a curve of Curves.elasticInOut.

See also:

 *  Theme, which AnimatedTheme uses to actually apply the interpolated theme.
 *  ThemeData, which describes the actual configuration of a theme.
 *  MaterialApp, which includes an AnimatedTheme widget configured via the MaterialApp.theme argument.

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatefulWidget
 *  ImplicitlyAnimatedWidget
 *  AnimatedTheme

## Constructors ##

AnimatedTheme(\{Key key, @required ThemeData data, bool isMaterialAppTheme: false, Curve curve: Curves.linear, Duration duration: kThemeAnimationDuration, VoidCallback onEnd, @required Widget child\})

Creates an animated theme. \[...\]

const

## Properties ##

child → Widget

The widget below this widget in the tree. \[...\]

final

curve → Curve

The curve to apply when animating the parameters of this container.

final, inherited

data → ThemeData

Specifies the color and typography values for descendant widgets.

final

duration → Duration

The duration over which to animate the parameters of this container.

final, inherited

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

isMaterialAppTheme → bool

True if this theme was created by the MaterialApp. See Theme.isMaterialAppTheme.

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

## Methods ##

createElement() → StatefulElement

Creates a StatefulElement to manage this widget's location in the tree. \[...\]

inherited

createState() → \_AnimatedThemeState

Creates the mutable state for this widget at a given location in the tree. \[...\]

override

debugDescribeChildren() → List<DiagnosticsNode>

Returns a list of DiagnosticsNode objects describing this node's children. \[...\]

@protected, inherited

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/theme.dart#L221