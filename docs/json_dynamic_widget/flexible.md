[*description*][description]

# Flexible class #

A widget that controls how a child of a Row, Column, or Flex flexes.

Using a Flexible widget gives a child of a Row, Column, or Flex the flexibility to expand to fill the available space in the main axis (e.g., horizontally for a Row or vertically for a Column), but, unlike Expanded, Flexible does not require the child to fill the available space.

A Flexible widget must be a descendant of a Row, Column, or Flex, and the path from the Flexible widget to its enclosing Row, Column, or Flex must contain only StatelessWidgets or StatefulWidgets (not other kinds of widgets, like RenderObjectWidgets).

See also:

 *  Expanded, which forces the child to expand to fill the available space.
 *  Spacer, a widget that takes up space proportional to its flex value.
 *  The [catalog of layout widgets][].

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  ProxyWidget
 *  ParentDataWidget<FlexParentData>
 *  Flexible

Implementers

 *  Expanded

## Constructors ##

Flexible(\{Key key, int flex: 1, FlexFit fit: FlexFit.loose, @required Widget child\})

Creates a widget that controls how a child of a Row, Column, or Flex flexes.

const

## Properties ##

child → Widget

The widget below this widget in the tree. \[...\]

final, inherited

debugTypicalAncestorWidgetClass → Type

The RenderObjectWidget that is typically used to set up the ParentData that applyParentData will write to. \[...\]

read-only, override

fit → FlexFit

How a flexible child is inscribed into the available space. \[...\]

final

flex → int

The flex factor to use for this child. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

applyParentData(RenderObject renderObject) → void

Write the data from this widget into the given render object's parent data. \[...\]

override

createElement() → ParentDataElement<FlexParentData>

Inflates this configuration to a concrete instance. \[...\]

inherited

debugCanApplyOutOfTurn() → bool

Whether the ParentDataElement.applyWidgetOutOfTurn method is allowed with this widget. \[...\]

@protected, inherited

debugDescribeChildren() → List<DiagnosticsNode>

Returns a list of DiagnosticsNode objects describing this node's children. \[...\]

@protected, inherited

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

override

debugIsValidRenderObject(RenderObject renderObject) → bool

Checks if this widget can apply its parent data to the provided `renderObject`. \[...\]

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/basic.dart#L4516
[catalog of layout widgets]: https://flutter.dev/widgets/layout/