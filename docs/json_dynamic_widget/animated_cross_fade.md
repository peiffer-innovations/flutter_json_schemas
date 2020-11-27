[*description*][description]

# AnimatedCrossFade class #

A widget that cross-fades between two given children and animates itself between their sizes.

The animation is controlled through the crossFadeState parameter. firstCurve and secondCurve represent the opacity curves of the two children. The firstCurve is inverted, i.e. it fades out when providing a growing curve like Curves.linear. The sizeCurve is the curve used to animate between the size of the fading-out child and the size of the fading-in child.

This widget is intended to be used to fade a pair of widgets with the same width. In the case where the two children have different heights, the animation crops overflowing children during the animation by aligning their top edge, which means that the bottom will be clipped.

The animation is automatically triggered when an existing AnimatedCrossFade is rebuilt with a different value for the crossFadeState property.

 *link* 

Sample

This code fades between two representations of the Flutter logo. It depends on a boolean field `_first`; when `_first` is true, the first logo is shown, otherwise the second logo is shown. When the field changes state, the AnimatedCrossFade widget cross-fades between the two forms of the logo over three seconds.

*assignment*

    AnimatedCrossFade(
      duration: const Duration(seconds: 3),
      firstChild: const FlutterLogo(style: FlutterLogoStyle.horizontal, size: 100.0),
      secondChild: const FlutterLogo(style: FlutterLogoStyle.stacked, size: 100.0),
      crossFadeState: _first ? CrossFadeState.showFirst : CrossFadeState.showSecond,
    )

See also:

 *  AnimatedOpacity, which fades between nothing and a single child.
 *  AnimatedSwitcher, which switches out a child for a new one with a customizable transition, supporting multiple cross-fades at once.
 *  AnimatedSize, the lower-level widget which AnimatedCrossFade uses to automatically change size.

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatefulWidget
 *  AnimatedCrossFade

## Constructors ##

AnimatedCrossFade(\{Key key, @required Widget firstChild, @required Widget secondChild, Curve firstCurve: Curves.linear, Curve secondCurve: Curves.linear, Curve sizeCurve: Curves.linear, AlignmentGeometry alignment: Alignment.topCenter, @required CrossFadeState crossFadeState, @required Duration duration, Duration reverseDuration, AnimatedCrossFadeBuilder layoutBuilder: defaultLayoutBuilder\})

Creates a cross-fade animation widget. \[...\]

const

## Properties ##

alignment → AlignmentGeometry

How the children should be aligned while the size is animating. \[...\]

final

crossFadeState → CrossFadeState

The child that will be shown when the animation has completed.

final

duration → Duration

The duration of the whole orchestrated animation.

final

firstChild → Widget

The child that is visible when crossFadeState is CrossFadeState.showFirst. It fades out when transitioning crossFadeState from CrossFadeState.showFirst to CrossFadeState.showSecond and vice versa.

final

firstCurve → Curve

The fade curve of the first child. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

layoutBuilder → AnimatedCrossFadeBuilder

A builder that positions the firstChild and secondChild widgets. \[...\]

final

reverseDuration → Duration

The duration of the whole orchestrated animation when running in reverse. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

secondChild → Widget

The child that is visible when crossFadeState is CrossFadeState.showSecond. It fades in when transitioning crossFadeState from CrossFadeState.showFirst to CrossFadeState.showSecond and vice versa.

final

secondCurve → Curve

The fade curve of the second child. \[...\]

final

sizeCurve → Curve

The curve of the animation between the two children's sizes. \[...\]

final

## Methods ##

createElement() → StatefulElement

Creates a StatefulElement to manage this widget's location in the tree. \[...\]

inherited

createState() → \_AnimatedCrossFadeState

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

## Static Methods ##

defaultLayoutBuilder(Widget topChild, Key topChildKey, Widget bottomChild, Key bottomChildKey) → Widget

The default layout algorithm used by AnimatedCrossFade. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/animated_cross_fade.dart#L114