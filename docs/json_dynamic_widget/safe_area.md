[*description*][description]

# SafeArea class #

A widget that insets its child by sufficient padding to avoid intrusions by the operating system.

For example, this will indent the child by enough to avoid the status bar at the top of the screen.

It will also indent the child by the amount necessary to avoid The Notch on the iPhone X, or other similar creative physical features of the display.

When a minimum padding is specified, the greater of the minimum padding or the safe area padding will be applied.

See also:

 *  SliverSafeArea, for insetting slivers to avoid operating system intrusions.
 *  Padding, for insetting widgets in general.
 *  MediaQuery, from which the window padding is obtained.
 *  dart:ui.Window.padding, which reports the padding from the operating system.

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatelessWidget
 *  SafeArea

## Constructors ##

SafeArea(\{Key key, bool left: true, bool top: true, bool right: true, bool bottom: true, EdgeInsets minimum: EdgeInsets.zero, bool maintainBottomViewPadding: false, @required Widget child\})

Creates a widget that avoids operating system interfaces. \[...\]

const

## Properties ##

bottom → bool

Whether to avoid system intrusions on the bottom side of the screen.

final

child → Widget

The widget below this widget in the tree. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

left → bool

Whether to avoid system intrusions on the left.

final

maintainBottomViewPadding → bool

Specifies whether the SafeArea should maintain the MediaQueryData.viewPadding instead of the MediaQueryData.padding when consumed by the MediaQueryData.viewInsets of the current context's MediaQuery, defaults to false. \[...\]

final

minimum → EdgeInsets

This minimum padding to apply. \[...\]

final

right → bool

Whether to avoid system intrusions on the right.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

top → bool

Whether to avoid system intrusions at the top of the screen, typically the system status bar.

final

## Methods ##

build(BuildContext context) → Widget

Describes the part of the user interface represented by this widget. \[...\]

override

createElement() → StatelessElement

Creates a StatelessElement to manage this widget's location in the tree. \[...\]

inherited

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/safe_area.dart#L38