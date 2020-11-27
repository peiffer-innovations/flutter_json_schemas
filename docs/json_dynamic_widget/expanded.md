[*description*][description]

# Expanded class #

A widget that expands a child of a Row, Column, or Flex so that the child fills the available space.

Using an Expanded widget makes a child of a Row, Column, or Flex expand to fill the available space along the main axis (e.g., horizontally for a Row or vertically for a Column). If multiple children are expanded, the available space is divided among them according to the flex factor.

An Expanded widget must be a descendant of a Row, Column, or Flex, and the path from the Expanded widget to its enclosing Row, Column, or Flex must contain only StatelessWidgets or StatefulWidgets (not other kinds of widgets, like RenderObjectWidgets).

 *link* 

Interactive App Sample code

This example shows how to use an Expanded widget in a Column so that its middle child, a Container here, expands to fill the space.

![This results in two thin blue boxes with a larger amber box in between.][]

To create a local project with this code sample, run:  
flutter create --sample=widgets.Expanded.1 mysample

This example shows how to use an Expanded widget in a Column so that its middle child, a Container here, expands to fill the space.

![This results in two thin blue boxes with a larger amber box in between.][]

*assignment*

    Widget build(BuildContext context) {
      return Scaffold(
        appBar: AppBar(
          title: Text('Expanded Column Sample'),
        ),
        body: Center(
           child: Column(
            children: <Widget>[
              Container(
                color: Colors.blue,
                height: 100,
                width: 100,
              ),
              Expanded(
                child: Container(
                  color: Colors.amber,
                  width: 100,
                ),
              ),
              Container(
                color: Colors.blue,
                height: 100,
                width: 100,
              ),
            ],
          ),
        ),
      );
    }

 *link* 

Interactive App Sample code

This example shows how to use an Expanded widget in a Row with multiple children expanded, utilizing the flex factor to prioritize available space.

![This results in a wide amber box, followed by a thin blue box, with a medium width amber box at the end.][This results in a wide amber box_ followed by a thin blue box_ with a medium width amber box at the end.]

To create a local project with this code sample, run:  
flutter create --sample=widgets.Expanded.2 mysample

This example shows how to use an Expanded widget in a Row with multiple children expanded, utilizing the flex factor to prioritize available space.

![This results in a wide amber box, followed by a thin blue box, with a medium width amber box at the end.][This results in a wide amber box_ followed by a thin blue box_ with a medium width amber box at the end.]

*assignment*

    Widget build(BuildContext context) {
      return Scaffold(
        appBar: AppBar(
          title: Text('Expanded Row Sample'),
        ),
        body: Center(
          child: Row(
            children: <Widget>[
              Expanded(
                flex: 2,
                child: Container(
                  color: Colors.amber,
                  height: 100,
                ),
              ),
              Container(
                color: Colors.blue,
                height: 100,
                width: 50,
              ),
              Expanded(
                flex: 1,
                child: Container(
                  color: Colors.amber,
                  height: 100,
                ),
              ),
            ],
          ),
        ),
      );
    }

See also:

 *  Flexible, which does not force the child to fill the available space.
 *  Spacer, a widget that takes up space proportional to its flex value.
 *  The [catalog of layout widgets][].

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  ProxyWidget
 *  ParentDataWidget<FlexParentData>
 *  Flexible
 *  Expanded

## Constructors ##

Expanded(\{Key key, int flex: 1, @required Widget child\})

Creates a widget that expands a child of a Row, Column, or Flex so that the child fills the available space along the flex widget's main axis.

const

## Properties ##

child → Widget

The widget below this widget in the tree. \[...\]

final, inherited

debugTypicalAncestorWidgetClass → Type

The RenderObjectWidget that is typically used to set up the ParentData that applyParentData will write to. \[...\]

read-only, inherited

fit → FlexFit

How a flexible child is inscribed into the available space. \[...\]

final, inherited

flex → int

The flex factor to use for this child. \[...\]

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

## Methods ##

applyParentData(RenderObject renderObject) → void

Write the data from this widget into the given render object's parent data. \[...\]

inherited

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

inherited

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/basic.dart#L4677
[This results in two thin blue boxes with a larger amber box in between.]: https://flutter.github.io/assets-for-api-docs/assets/widgets/expanded_column.png
[This results in a wide amber box_ followed by a thin blue box_ with a medium width amber box at the end.]: https://flutter.github.io/assets-for-api-docs/assets/widgets/expanded_row.png
[catalog of layout widgets]: https://flutter.dev/widgets/layout/