[*description*][description]

# Column class #

A widget that displays its children in a vertical array.

To cause a child to expand to fill the available vertical space, wrap the child in an Expanded widget.

The Column widget does not scroll (and in general it is considered an error to have more children in a Column than will fit in the available room). If you have a line of widgets and want them to be able to scroll if there is insufficient room, consider using a ListView.

For a horizontal variant, see Row.

If you only have one child, then consider using Align or Center to position the child.

 *link* 

Sample

This example uses a Column to arrange three widgets vertically, the last being made to fill all the remaining space.

![Using the Column in this way creates two short lines of text with a large Flutter underneath.][]

*assignment*

    Column(
      children: <Widget>[
        Text('Deliver features faster'),
        Text('Craft beautiful UIs'),
        Expanded(
          child: FittedBox(
            fit: BoxFit.contain, // otherwise the logo will be tiny
            child: const FlutterLogo(),
          ),
        ),
      ],
    )

 *link* 

Sample

In the sample above, the text and the logo are centered on each line. In the following example, the crossAxisAlignment is set to CrossAxisAlignment.start, so that the children are left-aligned. The mainAxisSize is set to MainAxisSize.min, so that the column shrinks to fit the children.

![column_properties.png][]

*assignment*

    Column(
      crossAxisAlignment: CrossAxisAlignment.start,
      mainAxisSize: MainAxisSize.min,
      children: <Widget>[
        Text('We move under cover and we move as one'),
        Text('Through the night, we have one shot to live another day'),
        Text('We cannot let a stray gunshot give us away'),
        Text('We will fight up close, seize the moment and stay in it'),
        Text('It’s either that or meet the business end of a bayonet'),
        Text('The code word is ‘Rochambeau,’ dig me?'),
        Text('Rochambeau!', style: DefaultTextStyle.of(context).style.apply(fontSizeFactor: 2.0)),
      ],
    )

## Troubleshooting ##

### When the incoming vertical constraints are unbounded ###

When a Column has one or more Expanded or Flexible children, and is placed in another Column, or in a ListView, or in some other context that does not provide a maximum height constraint for the Column, you will get an exception at runtime saying that there are children with non-zero flex but the vertical constraints are unbounded.

The problem, as described in the details that accompany that exception, is that using Flexible or Expanded means that the remaining space after laying out all the other children must be shared equally, but if the incoming vertical constraints are unbounded, there is infinite remaining space.

The key to solving this problem is usually to determine why the Column is receiving unbounded vertical constraints.

One common reason for this to happen is that the Column has been placed in another Column (without using Expanded or Flexible around the inner nested Column). When a Column lays out its non-flex children (those that have neither Expanded or Flexible around them), it gives them unbounded constraints so that they can determine their own dimensions (passing unbounded constraints usually signals to the child that it should shrink-wrap its contents). The solution in this case is typically to just wrap the inner column in an Expanded to indicate that it should take the remaining space of the outer column, rather than being allowed to take any amount of room it desires.

Another reason for this message to be displayed is nesting a Column inside a ListView or other vertical scrollable. In that scenario, there really is infinite vertical space (the whole point of a vertical scrolling list is to allow infinite space vertically). In such scenarios, it is usually worth examining why the inner Column should have an Expanded or Flexible child: what size should the inner children really be? The solution in this case is typically to remove the Expanded or Flexible widgets from around the inner children.

For more discussion about constraints, see BoxConstraints.

### The yellow and black striped banner ###

When the contents of a Column exceed the amount of space available, the Column overflows, and the contents are clipped. In debug mode, a yellow and black striped bar is rendered at the overflowing edge to indicate the problem, and a message is printed below the Column saying how much overflow was detected.

The usual solution is to use a ListView rather than a Column, to enable the contents to scroll when vertical space is limited.

## Layout algorithm ##

*This section describes how a Column is rendered by the framework.* *See BoxConstraints for an introduction to box layout models.*

Layout for a Column proceeds in six steps:

1.  Layout each child a null or zero flex factor (e.g., those that are not Expanded) with unbounded vertical constraints and the incoming horizontal constraints. If the crossAxisAlignment is CrossAxisAlignment.stretch, instead use tight horizontal constraints that match the incoming max width.
2.  Divide the remaining vertical space among the children with non-zero flex factors (e.g., those that are Expanded) according to their flex factor. For example, a child with a flex factor of 2.0 will receive twice the amount of vertical space as a child with a flex factor of 1.0.
3.  Layout each of the remaining children with the same horizontal constraints as in step 1, but instead of using unbounded vertical constraints, use vertical constraints based on the amount of space allocated in step 2. Children with Flexible.fit properties that are FlexFit.tight are given tight constraints (i.e., forced to fill the allocated space), and children with Flexible.fit properties that are FlexFit.loose are given loose constraints (i.e., not forced to fill the allocated space).
4.  The width of the Column is the maximum width of the children (which will always satisfy the incoming horizontal constraints).
5.  The height of the Column is determined by the mainAxisSize property. If the mainAxisSize property is MainAxisSize.max, then the height of the Column is the max height of the incoming constraints. If the mainAxisSize property is MainAxisSize.min, then the height of the Column is the sum of heights of the children (subject to the incoming constraints).
6.  Determine the position for each child according to the mainAxisAlignment and the crossAxisAlignment. For example, if the mainAxisAlignment is MainAxisAlignment.spaceBetween, any vertical space that has not been allocated to children is divided evenly and placed between the children.

See also:

 *  Row, for a horizontal equivalent.
 *  Flex, if you don't know in advance if you want a horizontal or vertical arrangement.
 *  Expanded, to indicate children that should take all the remaining room.
 *  Flexible, to indicate children that should share the remaining room but that may size smaller (leaving some remaining room unused).
 *  SingleChildScrollView, whose documentation discusses some ways to use a Column inside a scrolling container.
 *  Spacer, a widget that takes up space proportional to its flex value.
 *  The [catalog of layout widgets][].

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  RenderObjectWidget
 *  MultiChildRenderObjectWidget
 *  Flex
 *  Column

## Constructors ##

Column(\{Key key, MainAxisAlignment mainAxisAlignment: MainAxisAlignment.start, MainAxisSize mainAxisSize: MainAxisSize.max, CrossAxisAlignment crossAxisAlignment: CrossAxisAlignment.center, TextDirection textDirection, VerticalDirection verticalDirection: VerticalDirection.down, TextBaseline textBaseline, List<Widget> children: const <Widget>\[\]\})

Creates a vertical array of children. \[...\]

## Properties ##

children → List<Widget>

The widgets below this widget in the tree. \[...\]

final, inherited

clipBehavior → Clip

The content will be clipped (or not) according to this option. \[...\]

final, inherited

crossAxisAlignment → CrossAxisAlignment

How the children should be placed along the cross axis. \[...\]

final, inherited

direction → Axis

The direction to use as the main axis. \[...\]

final, inherited

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

mainAxisAlignment → MainAxisAlignment

How the children should be placed along the main axis. \[...\]

final, inherited

mainAxisSize → MainAxisSize

How much space should be occupied in the main axis. \[...\]

final, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

textBaseline → TextBaseline

If aligning items according to their baseline, which baseline to use. \[...\]

final, inherited

textDirection → TextDirection

Determines the order to lay children out horizontally and how to interpret `start` and `end` in the horizontal direction. \[...\]

final, inherited

verticalDirection → VerticalDirection

Determines the order to lay children out vertically and how to interpret `start` and `end` in the vertical direction. \[...\]

final, inherited

## Methods ##

createElement() → MultiChildRenderObjectElement

RenderObjectWidgets always inflate to a RenderObjectElement subclass.

inherited

createRenderObject(BuildContext context) → RenderFlex

Creates an instance of the RenderObject class that this RenderObjectWidget represents, using the configuration described by this RenderObjectWidget. \[...\]

inherited

debugDescribeChildren() → List<DiagnosticsNode>

Returns a list of DiagnosticsNode objects describing this node's children. \[...\]

@protected, inherited

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

inherited

didUnmountRenderObject(covariant RenderObject renderObject) → void

A render object previously associated with this widget has been removed from the tree. The given RenderObject will be of the same type as returned by this object's createRenderObject.

@protected, inherited

getEffectiveTextDirection(BuildContext context) → TextDirection

The value to pass to RenderFlex.textDirection. \[...\]

@protected, inherited

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

updateRenderObject(BuildContext context, covariant RenderFlex renderObject) → void

Copies the configuration described by this RenderObjectWidget to the given RenderObject, which will be of the same type as returned by this object's createRenderObject. \[...\]

inherited

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

@nonVirtual, inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/basic.dart#L4462
[Using the Column in this way creates two short lines of text with a large Flutter underneath.]: https://flutter.github.io/assets-for-api-docs/assets/widgets/column.png
[column_properties.png]: https://flutter.github.io/assets-for-api-docs/assets/widgets/column_properties.png
[catalog of layout widgets]: https://flutter.dev/widgets/layout/