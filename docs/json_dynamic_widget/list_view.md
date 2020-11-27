[*description*][description]

# ListView class #

A scrollable list of widgets arranged linearly.

ListView is the most commonly used scrolling widget. It displays its children one after another in the scroll direction. In the cross axis, the children are required to fill the ListView.

If non-null, the itemExtent forces the children to have the given extent in the scroll direction. Specifying an itemExtent is more efficient than letting the children determine their own extent because the scrolling machinery can make use of the foreknowledge of the children's extent to save work, for example when the scroll position changes drastically.

There are four options for constructing a ListView:

1.  The default constructor takes an explicit List<Widget> of children. This constructor is appropriate for list views with a small number of children because constructing the List requires doing work for every child that could possibly be displayed in the list view instead of just those children that are actually visible.
2.  The ListView.builder constructor takes an IndexedWidgetBuilder, which builds the children on demand. This constructor is appropriate for list views with a large (or infinite) number of children because the builder is called only for those children that are actually visible.
3.  The ListView.separated constructor takes two IndexedWidgetBuilders: `itemBuilder` builds child items on demand, and `separatorBuilder` similarly builds separator children which appear in between the child items. This constructor is appropriate for list views with a fixed number of children.
4.  The ListView.custom constructor takes a SliverChildDelegate, which provides the ability to customize additional aspects of the child model. For example, a SliverChildDelegate can control the algorithm used to estimate the size of children that are not actually visible.

To control the initial scroll offset of the scroll view, provide a controller with its ScrollController.initialScrollOffset property set.

By default, ListView will automatically pad the list's scrollable extremities to avoid partial obstructions indicated by MediaQuery's padding. To avoid this behavior, override with a zero padding property.

 *link* 

Sample

This example uses the default constructor for ListView which takes an explicit List<Widget> of children. This ListView's children are made up of Containers with Text.

![A ListView of 3 amber colored containers with sample text.][]

*assignment*

    ListView(
      padding: const EdgeInsets.all(8),
      children: <Widget>[
        Container(
          height: 50,
          color: Colors.amber[600],
          child: const Center(child: Text('Entry A')),
        ),
        Container(
          height: 50,
          color: Colors.amber[500],
          child: const Center(child: Text('Entry B')),
        ),
        Container(
          height: 50,
          color: Colors.amber[100],
          child: const Center(child: Text('Entry C')),
        ),
      ],
    )

 *link* 

Sample

This example mirrors the previous one, creating the same list using the ListView.builder constructor. Using the IndexedWidgetBuilder, children are built lazily and can be infinite in number.

![A ListView of 3 amber colored containers with sample text.][A ListView of 3 amber colored containers with sample text. 1]

*assignment*

    final List<String> entries = <String>['A', 'B', 'C'];
    final List<int> colorCodes = <int>[600, 500, 100];
    
    ListView.builder(
      padding: const EdgeInsets.all(8),
      itemCount: entries.length,
      itemBuilder: (BuildContext context, int index) {
        return Container(
          height: 50,
          color: Colors.amber[colorCodes[index]],
          child: Center(child: Text('Entry ${entries[index]}')),
        );
      }
    );

 *link* 

Sample

This example continues to build from our the previous ones, creating a similar list using ListView.separated. Here, a Divider is used as a separator.

![A ListView of 3 amber colored containers with sample text and a Divider between each of them.][]

*assignment*

    final List<String> entries = <String>['A', 'B', 'C'];
    final List<int> colorCodes = <int>[600, 500, 100];
    
    ListView.separated(
      padding: const EdgeInsets.all(8),
      itemCount: entries.length,
      itemBuilder: (BuildContext context, int index) {
        return Container(
          height: 50,
          color: Colors.amber[colorCodes[index]],
          child: Center(child: Text('Entry ${entries[index]}')),
        );
      },
      separatorBuilder: (BuildContext context, int index) => const Divider(),
    );

## Child elements' lifecycle ##

### Creation ###

While laying out the list, visible children's elements, states and render objects will be created lazily based on existing widgets (such as when using the default constructor) or lazily provided ones (such as when using the ListView.builder constructor).

### Destruction ###

When a child is scrolled out of view, the associated element subtree, states and render objects are destroyed. A new child at the same position in the list will be lazily recreated along with new elements, states and render objects when it is scrolled back.

### Destruction mitigation ###

In order to preserve state as child elements are scrolled in and out of view, the following options are possible:

 *  Moving the ownership of non-trivial UI-state-driving business logic out of the list child subtree. For instance, if a list contains posts with their number of upvotes coming from a cached network response, store the list of posts and upvote number in a data model outside the list. Let the list child UI subtree be easily recreate-able from the source-of-truth model object. Use StatefulWidgets in the child widget subtree to store instantaneous UI state only.
 *  Letting KeepAlive be the root widget of the list child widget subtree that needs to be preserved. The KeepAlive widget marks the child subtree's top render object child for keepalive. When the associated top render object is scrolled out of view, the list keeps the child's render object (and by extension, its associated elements and states) in a cache list instead of destroying them. When scrolled back into view, the render object is repainted as-is (if it wasn't marked dirty in the interim).
    
    This only works if `addAutomaticKeepAlives` and `addRepaintBoundaries` are false since those parameters cause the ListView to wrap each child widget subtree with other widgets.
 *  Using AutomaticKeepAlive widgets (inserted by default when `addAutomaticKeepAlives` is true). AutomaticKeepAlive allows descendant widgets to control whether the subtree is actually kept alive or not. This behavior is in contrast with KeepAlive, which will unconditionally keep the subtree alive.
    
    As an example, the EditableText widget signals its list child element subtree to stay alive while its text field has input focus. If it doesn't have focus and no other descendants signaled for keepalive via a KeepAliveNotification, the list child element subtree will be destroyed when scrolled away.
    
    AutomaticKeepAlive descendants typically signal it to be kept alive by using the AutomaticKeepAliveClientMixin, then implementing the AutomaticKeepAliveClientMixin.wantKeepAlive getter and calling AutomaticKeepAliveClientMixin.updateKeepAlive.

## Transitioning to CustomScrollView ##

A ListView is basically a CustomScrollView with a single SliverList in its CustomScrollView.slivers property.

If ListView is no longer sufficient, for example because the scroll view is to have both a list and a grid, or because the list is to be combined with a SliverAppBar, etc, it is straight-forward to port code from using ListView to using CustomScrollView directly.

The key, scrollDirection, reverse, controller, primary, physics, and shrinkWrap properties on ListView map directly to the identically named properties on CustomScrollView.

The CustomScrollView.slivers property should be a list containing either a SliverList or a SliverFixedExtentList; the former if itemExtent on the ListView was null, and the latter if itemExtent was not null.

The childrenDelegate property on ListView corresponds to the SliverList.delegate (or SliverFixedExtentList.delegate) property. The ListView constructor's `children` argument corresponds to the childrenDelegate being a SliverChildListDelegate with that same argument. The ListView.builder constructor's `itemBuilder` and `itemCount` arguments correspond to the childrenDelegate being a SliverChildBuilderDelegate with the equivalent arguments.

The padding property corresponds to having a SliverPadding in the CustomScrollView.slivers property instead of the list itself, and having the SliverList instead be a child of the SliverPadding.

CustomScrollViews don't automatically avoid obstructions from MediaQuery like ListViews do. To reproduce the behavior, wrap the slivers in SliverSafeAreas.

Once code has been ported to use CustomScrollView, other slivers, such as SliverGrid or SliverAppBar, can be put in the CustomScrollView.slivers list.

 *link* 

Sample

Here are two brief snippets showing a ListView and its equivalent using CustomScrollView:

*assignment*

    ListView(
      shrinkWrap: true,
      padding: const EdgeInsets.all(20.0),
      children: <Widget>[
        const Text("I'm dedicating every day to you"),
        const Text('Domestic life was never quite my style'),
        const Text('When you smile, you knock me out, I fall apart'),
        const Text('And I thought I was so smart'),
      ],
    )

 *link* 

Sample

*assignment*

    CustomScrollView(
      shrinkWrap: true,
      slivers: <Widget>[
        SliverPadding(
          padding: const EdgeInsets.all(20.0),
          sliver: SliverList(
            delegate: SliverChildListDelegate(
              <Widget>[
                const Text("I'm dedicating every day to you"),
                const Text('Domestic life was never quite my style'),
                const Text('When you smile, you knock me out, I fall apart'),
                const Text('And I thought I was so smart'),
              ],
            ),
          ),
        ),
      ],
    )

## Special handling for an empty list ##

A common design pattern is to have a custom UI for an empty list. The best way to achieve this in Flutter is just conditionally replacing the ListView at build time with whatever widgets you need to show for the empty list state:

 *link* 

Sample

Example of simple empty list interface:

*assignment*

    Widget build(BuildContext context) {
      return Scaffold(
        appBar: AppBar(title: const Text('Empty List Test')),
        body: itemCount > 0
          ? ListView.builder(
              itemCount: itemCount,
              itemBuilder: (BuildContext context, int index) {
                return ListTile(
                  title: Text('Item ${index + 1}'),
                );
              },
            )
          : Center(child: const Text('No items')),
      );
    }

## Selection of list items ##

`ListView` has no built-in notion of a selected item or items. For a small example of how a caller might wire up basic item selection, see ListTile.selected.

See also:

 *  SingleChildScrollView, which is a scrollable widget that has a single child.
 *  PageView, which is a scrolling list of child widgets that are each the size of the viewport.
 *  GridView, which is a scrollable, 2D array of widgets.
 *  CustomScrollView, which is a scrollable widget that creates custom scroll effects using slivers.
 *  ListBody, which arranges its children in a similar manner, but without scrolling.
 *  ScrollNotification and NotificationListener, which can be used to watch the scroll position without using a ScrollController.
 *  The [catalog of layout widgets][].
 *  Cookbook: [Use lists][]
 *  Cookbook: [Work with long lists][]
 *  Cookbook: [Create a horizontal list][]
 *  Cookbook: [Create lists with different types of items][]
 *  Cookbook: [Implement swipe to dismiss][]

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatelessWidget
 *  ScrollView
 *  BoxScrollView
 *  ListView

## Constructors ##

ListView(\{Key key, Axis scrollDirection: Axis.vertical, bool reverse: false, ScrollController controller, bool primary, ScrollPhysics physics, bool shrinkWrap: false, EdgeInsetsGeometry padding, double itemExtent, bool addAutomaticKeepAlives: true, bool addRepaintBoundaries: true, bool addSemanticIndexes: true, double cacheExtent, List<Widget> children: const <Widget>\[\], int semanticChildCount, DragStartBehavior dragStartBehavior: DragStartBehavior.start, ScrollViewKeyboardDismissBehavior keyboardDismissBehavior: ScrollViewKeyboardDismissBehavior.manual, String restorationId, Clip clipBehavior: Clip.hardEdge\})

Creates a scrollable, linear array of widgets from an explicit List. \[...\]

ListView.builder(\{Key key, Axis scrollDirection: Axis.vertical, bool reverse: false, ScrollController controller, bool primary, ScrollPhysics physics, bool shrinkWrap: false, EdgeInsetsGeometry padding, double itemExtent, @required IndexedWidgetBuilder itemBuilder, int itemCount, bool addAutomaticKeepAlives: true, bool addRepaintBoundaries: true, bool addSemanticIndexes: true, double cacheExtent, int semanticChildCount, DragStartBehavior dragStartBehavior: DragStartBehavior.start, ScrollViewKeyboardDismissBehavior keyboardDismissBehavior: ScrollViewKeyboardDismissBehavior.manual, String restorationId, Clip clipBehavior: Clip.hardEdge\})

Creates a scrollable, linear array of widgets that are created on demand. \[...\]

ListView.custom(\{Key key, Axis scrollDirection: Axis.vertical, bool reverse: false, ScrollController controller, bool primary, ScrollPhysics physics, bool shrinkWrap: false, EdgeInsetsGeometry padding, double itemExtent, @required SliverChildDelegate childrenDelegate, double cacheExtent, int semanticChildCount, DragStartBehavior dragStartBehavior: DragStartBehavior.start, ScrollViewKeyboardDismissBehavior keyboardDismissBehavior: ScrollViewKeyboardDismissBehavior.manual, String restorationId, Clip clipBehavior: Clip.hardEdge\})

Creates a scrollable, linear array of widgets with a custom child model. \[...\]

const

ListView.separated(\{Key key, Axis scrollDirection: Axis.vertical, bool reverse: false, ScrollController controller, bool primary, ScrollPhysics physics, bool shrinkWrap: false, EdgeInsetsGeometry padding, @required IndexedWidgetBuilder itemBuilder, @required IndexedWidgetBuilder separatorBuilder, @required int itemCount, bool addAutomaticKeepAlives: true, bool addRepaintBoundaries: true, bool addSemanticIndexes: true, double cacheExtent, DragStartBehavior dragStartBehavior: DragStartBehavior.start, ScrollViewKeyboardDismissBehavior keyboardDismissBehavior: ScrollViewKeyboardDismissBehavior.manual, String restorationId, Clip clipBehavior: Clip.hardEdge\})

Creates a fixed-length scrollable linear array of list "items" separated by list item "separators". \[...\]

## Properties ##

anchor → double

The relative position of the zero scroll offset. \[...\]

final, inherited

cacheExtent → double

The viewport has an area before and after the visible area to cache items that are about to become visible when the user scrolls. \[...\]

final, inherited

center → Key

The first child in the GrowthDirection.forward growth direction. \[...\]

final, inherited

childrenDelegate → SliverChildDelegate

A delegate that provides the children for the ListView. \[...\]

final

clipBehavior → Clip

The content will be clipped (or not) according to this option. \[...\]

final, inherited

controller → ScrollController

An object that can be used to control the position to which this scroll view is scrolled. \[...\]

final, inherited

dragStartBehavior → DragStartBehavior

Determines the way that drag start behavior is handled. \[...\]

final, inherited

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

itemExtent → double

If non-null, forces the children to have the given extent in the scroll direction. \[...\]

final

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

keyboardDismissBehavior → ScrollViewKeyboardDismissBehavior

ScrollViewKeyboardDismissBehavior the defines how this ScrollView will dismiss the keyboard automatically.

final, inherited

padding → EdgeInsetsGeometry

The amount of space by which to inset the children.

final, inherited

physics → ScrollPhysics

How the scroll view should respond to user input. \[...\]

final, inherited

primary → bool

Whether this is the primary scroll view associated with the parent PrimaryScrollController. \[...\]

final, inherited

restorationId → String

Restoration ID to save and restore the scroll offset of the scrollable. \[...\]

final, inherited

reverse → bool

Whether the scroll view scrolls in the reading direction. \[...\]

final, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

scrollDirection → Axis

The axis along which the scroll view scrolls. \[...\]

final, inherited

semanticChildCount → int

The number of children that will contribute semantic information. \[...\]

final, inherited

shrinkWrap → bool

Whether the extent of the scroll view in the scrollDirection should be determined by the contents being viewed. \[...\]

final, inherited

## Methods ##

build(BuildContext context) → Widget

Describes the part of the user interface represented by this widget. \[...\]

inherited

buildChildLayout(BuildContext context) → Widget

Subclasses should override this method to build the layout model.

override

buildSlivers(BuildContext context) → List<Widget>

Build the list of widgets to place inside the viewport. \[...\]

inherited

buildViewport(BuildContext context, ViewportOffset offset, AxisDirection axisDirection, List<Widget> slivers) → Widget

Build the viewport. \[...\]

@protected, inherited

createElement() → StatelessElement

Creates a StatelessElement to manage this widget's location in the tree. \[...\]

inherited

debugDescribeChildren() → List<DiagnosticsNode>

Returns a list of DiagnosticsNode objects describing this node's children. \[...\]

@protected, inherited

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

override

getDirection(BuildContext context) → AxisDirection

Returns the AxisDirection in which the scroll view scrolls. \[...\]

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

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

@nonVirtual, inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/scroll_view.dart#L1038
[A ListView of 3 amber colored containers with sample text.]: https://flutter.github.io/assets-for-api-docs/assets/widgets/list_view.png
[A ListView of 3 amber colored containers with sample text. 1]: https://flutter.github.io/assets-for-api-docs/assets/widgets/list_view_builder.png
[A ListView of 3 amber colored containers with sample text and a Divider between each of them.]: https://flutter.github.io/assets-for-api-docs/assets/widgets/list_view_separated.png
[catalog of layout widgets]: https://flutter.dev/widgets/layout/
[Use lists]: https://flutter.dev/docs/cookbook/lists/basic-list
[Work with long lists]: https://flutter.dev/docs/cookbook/lists/long-lists
[Create a horizontal list]: https://flutter.dev/docs/cookbook/lists/horizontal-list
[Create lists with different types of items]: https://flutter.dev/docs/cookbook/lists/mixed-list
[Implement swipe to dismiss]: https://flutter.dev/docs/cookbook/gestures/dismissible