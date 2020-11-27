[*description*][description]

# Row class #

A widget that displays its children in a horizontal array.

To cause a child to expand to fill the available horizontal space, wrap the child in an Expanded widget.

The Row widget does not scroll (and in general it is considered an error to have more children in a Row than will fit in the available room). If you have a line of widgets and want them to be able to scroll if there is insufficient room, consider using a ListView.

For a vertical variant, see Column.

If you only have one child, then consider using Align or Center to position the child.

 *link* 

Sample

This example divides the available space into three (horizontally), and places text centered in the first two cells and the Flutter logo centered in the third:

![row.png][]

*assignment*

    Row(
      children: <Widget>[
        Expanded(
          child: Text('Deliver features faster', textAlign: TextAlign.center),
        ),
        Expanded(
          child: Text('Craft beautiful UIs', textAlign: TextAlign.center),
        ),
        Expanded(
          child: FittedBox(
            fit: BoxFit.contain, // otherwise the logo will be tiny
            child: const FlutterLogo(),
          ),
        ),
      ],
    )

## Troubleshooting ##

### Why does my row have a yellow and black warning stripe? ###

If the non-flexible contents of the row (those that are not wrapped in Expanded or Flexible widgets) are together wider than the row itself, then the row is said to have overflowed. When a row overflows, the row does not have any remaining space to share between its Expanded and Flexible children. The row reports this by drawing a yellow and black striped warning box on the edge that is overflowing. If there is room on the outside of the row, the amount of overflow is printed in red lettering.

#### Story time ####

Suppose, for instance, that you had this code:

    Row(
      children: <Widget>[
        const FlutterLogo(),
        const Text("Flutter's hot reload helps you quickly and easily experiment, build UIs, add features, and fix bug faster. Experience sub-second reload times, without losing state, on emulators, simulators, and hardware for iOS and Android."),
        const Icon(Icons.sentiment_very_satisfied),
      ],
    )

The row first asks its first child, the FlutterLogo, to lay out, at whatever size the logo would like. The logo is friendly and happily decides to be 24 pixels to a side. This leaves lots of room for the next child. The row then asks that next child, the text, to lay out, at whatever size it thinks is best.

At this point, the text, not knowing how wide is too wide, says "Ok, I will be thiiiiiiiiiiiiiiiiiiiis wide.", and goes well beyond the space that the row has available, not wrapping. The row responds, "That's not fair, now I have no more room available for my other children!", and gets angry and sprouts a yellow and black strip.

![row_error.png][]

The fix is to wrap the second child in an Expanded widget, which tells the row that the child should be given the remaining room:

    Row(
      children: <Widget>[
        const FlutterLogo(),
        const Expanded(
          child: Text("Flutter's hot reload helps you quickly and easily experiment, build UIs, add features, and fix bug faster. Experience sub-second reload times, without losing state, on emulators, simulators, and hardware for iOS and Android."),
        ),
        const Icon(Icons.sentiment_very_satisfied),
      ],
    )

Now, the row first asks the logo to lay out, and then asks the *icon* to lay out. The Icon, like the logo, is happy to take on a reasonable size (also 24 pixels, not coincidentally, since both FlutterLogo and Icon honor the ambient IconTheme). This leaves some room left over, and now the row tells the text exactly how wide to be: the exact width of the remaining space. The text, now happy to comply to a reasonable request, wraps the text within that width, and you end up with a paragraph split over several lines.

![row_fixed.png][]

The textDirection property controls the direction that children are rendered in. TextDirection.ltr is the default textDirection of Row children, so the first child is rendered at the `start` of the Row, to the left, with subsequent children following to the right. If you want to order children in the opposite direction (right to left), then textDirection can be set to TextDirection.rtl. This is shown in the example below

    Row(
      textDirection: TextDirection.rtl,
      children: <Widget>[
        const FlutterLogo(),
        const Expanded(
          child: Text("Flutter's hot reload helps you quickly and easily experiment, build UIs, add features, and fix bug faster. Experience sub-second reload times, without losing state, on emulators, simulators, and hardware for iOS and Android."),
        ),
        const Icon(Icons.sentiment_very_satisfied),
      ],
    )

![row_textDirection.png][]

## Layout algorithm ##

*This section describes how a Row is rendered by the framework.* *See BoxConstraints for an introduction to box layout models.*

Layout for a Row proceeds in six steps:

1.  Layout each child a null or zero flex factor (e.g., those that are not Expanded) with unbounded horizontal constraints and the incoming vertical constraints. If the crossAxisAlignment is CrossAxisAlignment.stretch, instead use tight vertical constraints that match the incoming max height.
2.  Divide the remaining horizontal space among the children with non-zero flex factors (e.g., those that are Expanded) according to their flex factor. For example, a child with a flex factor of 2.0 will receive twice the amount of horizontal space as a child with a flex factor of 1.0.
3.  Layout each of the remaining children with the same vertical constraints as in step 1, but instead of using unbounded horizontal constraints, use horizontal constraints based on the amount of space allocated in step 2. Children with Flexible.fit properties that are FlexFit.tight are given tight constraints (i.e., forced to fill the allocated space), and children with Flexible.fit properties that are FlexFit.loose are given loose constraints (i.e., not forced to fill the allocated space).
4.  The height of the Row is the maximum height of the children (which will always satisfy the incoming vertical constraints).
5.  The width of the Row is determined by the mainAxisSize property. If the mainAxisSize property is MainAxisSize.max, then the width of the Row is the max width of the incoming constraints. If the mainAxisSize property is MainAxisSize.min, then the width of the Row is the sum of widths of the children (subject to the incoming constraints).
6.  Determine the position for each child according to the mainAxisAlignment and the crossAxisAlignment. For example, if the mainAxisAlignment is MainAxisAlignment.spaceBetween, any horizontal space that has not been allocated to children is divided evenly and placed between the children.

See also:

 *  Column, for a vertical equivalent.
 *  Flex, if you don't know in advance if you want a horizontal or vertical arrangement.
 *  Expanded, to indicate children that should take all the remaining room.
 *  Flexible, to indicate children that should share the remaining room but that may by sized smaller (leaving some remaining room unused).
 *  Spacer, a widget that takes up space proportional to its flex value.
 *  The [catalog of layout widgets][].

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  RenderObjectWidget
 *  MultiChildRenderObjectWidget
 *  Flex
 *  Row

## Constructors ##

Row(\{Key key, MainAxisAlignment mainAxisAlignment: MainAxisAlignment.start, MainAxisSize mainAxisSize: MainAxisSize.max, CrossAxisAlignment crossAxisAlignment: CrossAxisAlignment.center, TextDirection textDirection, VerticalDirection verticalDirection: VerticalDirection.down, TextBaseline textBaseline: TextBaseline.alphabetic, List<Widget> children: const <Widget>\[\]\})

Creates a horizontal array of children. \[...\]

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/basic.dart#L4260
[row.png]: https://flutter.github.io/assets-for-api-docs/assets/widgets/row.png
[row_error.png]: https://flutter.github.io/assets-for-api-docs/assets/widgets/row_error.png
[row_fixed.png]: https://flutter.github.io/assets-for-api-docs/assets/widgets/row_fixed.png
[row_textDirection.png]: https://flutter.github.io/assets-for-api-docs/assets/widgets/row_textDirection.png
[catalog of layout widgets]: https://flutter.dev/widgets/layout/