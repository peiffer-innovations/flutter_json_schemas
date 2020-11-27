[*description*][description]

# AppBar class #

A material design app bar.

An app bar consists of a toolbar and potentially other widgets, such as a TabBar and a FlexibleSpaceBar. App bars typically expose one or more common actions with IconButtons which are optionally followed by a PopupMenuButton for less common operations (sometimes called the "overflow menu").

App bars are typically used in the Scaffold.appBar property, which places the app bar as a fixed-height widget at the top of the screen. For a scrollable app bar, see SliverAppBar, which embeds an AppBar in a sliver for use in a CustomScrollView.

The AppBar displays the toolbar widgets, leading, title, and actions, above the bottom (if any). The bottom is usually used for a TabBar. If a flexibleSpace widget is specified then it is stacked behind the toolbar and the bottom widget. The following diagram shows where each of these slots appears in the toolbar when the writing language is left-to-right (e.g. English):

The AppBar insets its content based on the ambient MediaQuery's padding, to avoid system UI intrusions. It's taken care of by Scaffold when used in the Scaffold.appBar property. When animating an AppBar, unexpected MediaQuery changes (as is common in Hero animations) may cause the content to suddenly jump. Wrap the AppBar in a MediaQuery widget, and adjust its padding such that the animation is smooth.

![The leading widget is in the top left, the actions are in the top right, the title is between them. The bottom is, naturally, at the bottom, and the flexibleSpace is behind all of them.][The leading widget is in the top left_ the actions are in the top right_ the title is between them. The bottom is_ naturally_ at the bottom_ and the flexibleSpace is behind all of them.]

If the leading widget is omitted, but the AppBar is in a Scaffold with a Drawer, then a button will be inserted to open the drawer. Otherwise, if the nearest Navigator has any previous routes, a BackButton is inserted instead. This behavior can be turned off by setting the automaticallyImplyLeading to false. In that case a null leading widget will result in the middle/title widget stretching to start.

 *link* 

Interactive App Sample code

This sample shows an AppBar with two simple actions. The first action opens a SnackBar, while the second action navigates to a new page.

To create a local project with this code sample, run:  
flutter create --sample=material.AppBar.1 mysample

This sample shows an AppBar with two simple actions. The first action opens a SnackBar, while the second action navigates to a new page.

*assignment*

    final GlobalKey<ScaffoldState> scaffoldKey = GlobalKey<ScaffoldState>();
    final SnackBar snackBar = const SnackBar(content: Text('Showing Snackbar'));
    
    void openPage(BuildContext context) {
      Navigator.push(context, MaterialPageRoute(
        builder: (BuildContext context) {
          return Scaffold(
            appBar: AppBar(
              title: const Text('Next page'),
            ),
            body: const Center(
              child: Text(
                'This is the next page',
                style: TextStyle(fontSize: 24),
              ),
            ),
          );
        },
      ));
    }
    
    // ...
    
    Widget build(BuildContext context) {
      return Scaffold(
        key: scaffoldKey,
        appBar: AppBar(
          title: const Text('AppBar Demo'),
          actions: <Widget>[
            IconButton(
              icon: const Icon(Icons.add_alert),
              tooltip: 'Show Snackbar',
              onPressed: () {
                scaffoldKey.currentState.showSnackBar(snackBar);
              },
            ),
            IconButton(
              icon: const Icon(Icons.navigate_next),
              tooltip: 'Next page',
              onPressed: () {
                openPage(context);
              },
            ),
          ],
        ),
        body: const Center(
          child: Text(
            'This is the home page',
            style: TextStyle(fontSize: 24),
          ),
        ),
      );
    }

See also:

 *  Scaffold, which displays the AppBar in its Scaffold.appBar slot.
 *  SliverAppBar, which uses AppBar to provide a flexible app bar that can be used in a CustomScrollView.
 *  TabBar, which is typically placed in the bottom slot of the AppBar if the screen has multiple pages arranged in tabs.
 *  IconButton, which is used with actions to show buttons on the app bar.
 *  PopupMenuButton, to show a popup menu on the app bar, via actions.
 *  FlexibleSpaceBar, which is used with flexibleSpace when the app bar can expand and collapse.
 *  [material.io/design/components/app-bars-top.html][material.io_design_components_app-bars-top.html]
 *  Cookbook: [Place a floating app bar above a list][]
 *  See our [AppBar Basics sample][] and our advanced samples with app bars with [tabs][] or [custom bottom widgets][].

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatefulWidget
 *  AppBar

Implemented types

 *  PreferredSizeWidget

## Constructors ##

AppBar(\{Key key, Widget leading, bool automaticallyImplyLeading: true, Widget title, List<Widget> actions, Widget flexibleSpace, PreferredSizeWidget bottom, double elevation, Color shadowColor, ShapeBorder shape, Color backgroundColor, Brightness brightness, IconThemeData iconTheme, IconThemeData actionsIconTheme, TextTheme textTheme, bool primary: true, bool centerTitle, bool excludeHeaderSemantics: false, double titleSpacing: NavigationToolbar.kMiddleSpacing, double toolbarOpacity: 1.0, double bottomOpacity: 1.0, double toolbarHeight, double leadingWidth\})

Creates a material design app bar. \[...\]

## Properties ##

actions → List<Widget>

Widgets to display in a row after the title widget. \[...\]

final

actionsIconTheme → IconThemeData

The color, opacity, and size to use for the icons that appear in the app bar's actions. This should only be used when the actions should be themed differently than the icon that appears in the app bar's leading widget. \[...\]

final

automaticallyImplyLeading → bool

Controls whether we should try to imply the leading widget if null. \[...\]

final

backgroundColor → Color

The color to use for the app bar's material. Typically this should be set along with brightness, iconTheme, textTheme. \[...\]

final

bottom → PreferredSizeWidget

This widget appears across the bottom of the app bar. \[...\]

final

bottomOpacity → double

How opaque the bottom part of the app bar is. \[...\]

final

brightness → Brightness

The brightness of the app bar's material. Typically this is set along with backgroundColor, iconTheme, textTheme. \[...\]

final

centerTitle → bool

Whether the title should be centered. \[...\]

final

elevation → double

The z-coordinate at which to place this app bar relative to its parent. \[...\]

final

excludeHeaderSemantics → bool

Whether the title should be wrapped with header Semantics. \[...\]

final

flexibleSpace → Widget

This widget is stacked behind the toolbar and the tab bar. It's height will be the same as the app bar's overall height. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

iconTheme → IconThemeData

The color, opacity, and size to use for app bar icons. Typically this is set along with backgroundColor, brightness, textTheme. \[...\]

final

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

leading → Widget

A widget to display before the title. \[...\]

final

leadingWidth → double

Defines the width of leading widget. \[...\]

final

preferredSize → Size

A size whose height is the sum of toolbarHeight and the bottom widget's preferred height. \[...\]

final

primary → bool

Whether this app bar is being displayed at the top of the screen. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

shadowColor → Color

The color to paint the shadow below the app bar. \[...\]

final

shape → ShapeBorder

The material's shape as well its shadow. \[...\]

final

textTheme → TextTheme

The typographic styles to use for text in the app bar. Typically this is set along with brightness backgroundColor, iconTheme. \[...\]

final

title → Widget

The primary widget displayed in the app bar. \[...\]

final

titleSpacing → double

The spacing around title content on the horizontal axis. This spacing is applied even if there is no leading content or actions. If you want title to take all the space available, set this value to 0.0. \[...\]

final

toolbarHeight → double

Defines the height of the toolbar component of an AppBar. \[...\]

final

toolbarOpacity → double

How opaque the toolbar part of the app bar is. \[...\]

final

## Methods ##

createElement() → StatefulElement

Creates a StatefulElement to manage this widget's location in the tree. \[...\]

inherited

createState() → \_AppBarState

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/app_bar.dart#L181
[The leading widget is in the top left_ the actions are in the top right_ the title is between them. The bottom is_ naturally_ at the bottom_ and the flexibleSpace is behind all of them.]: https://flutter.github.io/assets-for-api-docs/assets/material/app_bar.png
[material.io_design_components_app-bars-top.html]: https://material.io/design/components/app-bars-top.html
[Place a floating app bar above a list]: https://flutter.dev/docs/cookbook/lists/floating-app-bar
[AppBar Basics sample]: https://flutter.dev/docs/catalog/samples/basic-app-bar
[tabs]: https://flutter.dev/docs/catalog/samples/tabbed-app-bar
[custom bottom widgets]: https://flutter.dev/docs/catalog/samples/app-bar-bottom