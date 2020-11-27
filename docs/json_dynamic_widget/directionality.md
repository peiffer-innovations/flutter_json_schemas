[*description*][description]

# Directionality class #

A widget that determines the ambient directionality of text and text-direction-sensitive render objects.

For example, Padding depends on the Directionality to resolve EdgeInsetsDirectional objects into absolute EdgeInsets objects.

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  ProxyWidget
 *  InheritedWidget
 *  Directionality

## Constructors ##

Directionality(\{Key key, @required TextDirection textDirection, @required Widget child\})

Creates a widget that determines the directionality of text and text-direction-sensitive render objects. \[...\]

const

## Properties ##

child → Widget

The widget below this widget in the tree. \[...\]

final, inherited

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

textDirection → TextDirection

The text direction for this subtree.

final

## Methods ##

createElement() → InheritedElement

Inflates this configuration to a concrete instance. \[...\]

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

updateShouldNotify(covariant Directionality oldWidget) → bool

Whether the framework should notify widgets that inherit from this widget. \[...\]

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

@nonVirtual, inherited

## Static Methods ##

of(BuildContext context) → TextDirection

The text direction from the closest instance of this class that encloses the given context. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/basic.dart#L85