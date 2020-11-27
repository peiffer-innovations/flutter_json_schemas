[*description*][description]

# Scaffold class #

Implements the basic material design visual layout structure.

This class provides APIs for showing drawers, snack bars, and bottom sheets.

To display a snackbar or a persistent bottom sheet, obtain the ScaffoldState for the current BuildContext via Scaffold.of and use the ScaffoldState.showSnackBar and ScaffoldState.showBottomSheet functions.

 *link* 

Interactive App Sample code

This example shows a Scaffold with a body and FloatingActionButton. The body is a Text placed in a Center in order to center the text within the Scaffold. The FloatingActionButton is connected to a callback that increments a counter.

![The Scaffold has a white background with a blue AppBar at the top. A blue FloatingActionButton is positioned at the bottom right corner of the Scaffold.][]

To create a local project with this code sample, run:  
flutter create --sample=material.Scaffold.1 mysample

This example shows a Scaffold with a body and FloatingActionButton. The body is a Text placed in a Center in order to center the text within the Scaffold. The FloatingActionButton is connected to a callback that increments a counter.

![The Scaffold has a white background with a blue AppBar at the top. A blue FloatingActionButton is positioned at the bottom right corner of the Scaffold.][]

*assignment*

    int _count = 0;
    
    Widget build(BuildContext context) {
      return Scaffold(
        appBar: AppBar(
          title: const Text('Sample Code'),
        ),
        body: Center(
          child: Text('You have pressed the button $_count times.')
        ),
        floatingActionButton: FloatingActionButton(
          onPressed: () => setState(() => _count++),
          tooltip: 'Increment Counter',
          child: const Icon(Icons.add),
        ),
      );
    }

 *link* 

Interactive App Sample code

This example shows a Scaffold with a blueGrey backgroundColor, body and FloatingActionButton. The body is a Text placed in a Center in order to center the text within the Scaffold. The FloatingActionButton is connected to a callback that increments a counter.

![scaffold_background_color.png][]

To create a local project with this code sample, run:  
flutter create --sample=material.Scaffold.2 mysample

This example shows a Scaffold with a blueGrey backgroundColor, body and FloatingActionButton. The body is a Text placed in a Center in order to center the text within the Scaffold. The FloatingActionButton is connected to a callback that increments a counter.

![scaffold_background_color.png][]

*assignment*

    int _count = 0;
    
    Widget build(BuildContext context) {
      return Scaffold(
        appBar: AppBar(
          title: const Text('Sample Code'),
        ),
        body: Center(
          child: Text('You have pressed the button $_count times.')
        ),
        backgroundColor: Colors.blueGrey.shade200,
        floatingActionButton: FloatingActionButton(
          onPressed: () => setState(() => _count++),
          tooltip: 'Increment Counter',
          child: const Icon(Icons.add),
        ),
      );
    }

 *link* 

Interactive App Sample code

This example shows a Scaffold with an AppBar, a BottomAppBar and a FloatingActionButton. The body is a Text placed in a Center in order to center the text within the Scaffold. The FloatingActionButton is centered and docked within the BottomAppBar using FloatingActionButtonLocation.centerDocked. The FloatingActionButton is connected to a callback that increments a counter.

![scaffold_bottom_app_bar.png][]

To create a local project with this code sample, run:  
flutter create --sample=material.Scaffold.3 mysample

This example shows a Scaffold with an AppBar, a BottomAppBar and a FloatingActionButton. The body is a Text placed in a Center in order to center the text within the Scaffold. The FloatingActionButton is centered and docked within the BottomAppBar using FloatingActionButtonLocation.centerDocked. The FloatingActionButton is connected to a callback that increments a counter.

![scaffold_bottom_app_bar.png][]

*assignment*

    int _count = 0;
    
    Widget build(BuildContext context) {
      return Scaffold(
        appBar: AppBar(
          title: Text('Sample Code'),
        ),
        body: Center(
          child: Text('You have pressed the button $_count times.'),
        ),
        bottomNavigationBar: BottomAppBar(
          shape: const CircularNotchedRectangle(),
          child: Container(height: 50.0,),
        ),
        floatingActionButton: FloatingActionButton(
          onPressed: () => setState(() {
            _count++;
          }),
          tooltip: 'Increment Counter',
          child: Icon(Icons.add),
        ),
        floatingActionButtonLocation: FloatingActionButtonLocation.centerDocked,
      );
    }

## Scaffold layout, the keyboard, and display "notches" ##

The scaffold will expand to fill the available space. That usually means that it will occupy its entire window or device screen. When the device's keyboard appears the Scaffold's ancestor MediaQuery widget's MediaQueryData.viewInsets changes and the Scaffold will be rebuilt. By default the scaffold's body is resized to make room for the keyboard. To prevent the resize set resizeToAvoidBottomInset to false. In either case the focused widget will be scrolled into view if it's within a scrollable container.

The MediaQueryData.padding value defines areas that might not be completely visible, like the display "notch" on the iPhone X. The scaffold's body is not inset by this padding value although an appBar or bottomNavigationBar will typically cause the body to avoid the padding. The SafeArea widget can be used within the scaffold's body to avoid areas like display notches.

## Troubleshooting ##

### Nested Scaffolds ###

The Scaffold was designed to be the single top level container for a MaterialApp and it's typically not necessary to nest scaffolds. For example in a tabbed UI, where the bottomNavigationBar is a TabBar and the body is a TabBarView, you might be tempted to make each tab bar view a scaffold with a differently titled AppBar. It would be better to add a listener to the TabController that updates the AppBar.

 *link* 

Sample

Add a listener to the app's tab controller so that the AppBar title of the app's one and only scaffold is reset each time a new tab is selected.

*assignment*

    TabController(vsync: tickerProvider, length: tabCount)..addListener(() {
      if (!tabController.indexIsChanging) {
        setState(() {
          // Rebuild the enclosing scaffold with a new AppBar title
          appBarTitle = 'Tab ${tabController.index}';
        });
      }
    })

Although there are some use cases, like a presentation app that shows embedded flutter content, where nested scaffolds are appropriate, it's best to avoid nesting scaffolds.

See also:

 *  AppBar, which is a horizontal bar typically shown at the top of an app using the appBar property.
 *  BottomAppBar, which is a horizontal bar typically shown at the bottom of an app using the bottomNavigationBar property.
 *  FloatingActionButton, which is a circular button typically shown in the bottom right corner of the app using the floatingActionButton property.
 *  Drawer, which is a vertical panel that is typically displayed to the left of the body (and often hidden on phones) using the drawer property.
 *  BottomNavigationBar, which is a horizontal array of buttons typically shown along the bottom of the app using the bottomNavigationBar property.
 *  SnackBar, which is a temporary notification typically shown near the bottom of the app using the ScaffoldState.showSnackBar method.
 *  BottomSheet, which is an overlay typically shown near the bottom of the app. A bottom sheet can either be persistent, in which case it is shown using the ScaffoldState.showBottomSheet method, or modal, in which case it is shown using the showModalBottomSheet function.
 *  ScaffoldState, which is the state associated with this widget.
 *  [material.io/design/layout/responsive-layout-grid.html][material.io_design_layout_responsive-layout-grid.html]
 *  Cookbook: [Add a Drawer to a screen][]
 *  Cookbook: [Display a snackbar][]
 *  See our [Scaffold Sample Apps][].

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatefulWidget
 *  Scaffold

## Constructors ##

Scaffold(\{Key key, PreferredSizeWidget appBar, Widget body, Widget floatingActionButton, FloatingActionButtonLocation floatingActionButtonLocation, FloatingActionButtonAnimator floatingActionButtonAnimator, List<Widget> persistentFooterButtons, Widget drawer, Widget endDrawer, Widget bottomNavigationBar, Widget bottomSheet, Color backgroundColor, bool resizeToAvoidBottomPadding, bool resizeToAvoidBottomInset, bool primary: true, DragStartBehavior drawerDragStartBehavior: DragStartBehavior.start, bool extendBody: false, bool extendBodyBehindAppBar: false, Color drawerScrimColor, double drawerEdgeDragWidth, bool drawerEnableOpenDragGesture: true, bool endDrawerEnableOpenDragGesture: true\})

Creates a visual scaffold for material design widgets.

const

## Properties ##

appBar → PreferredSizeWidget

An app bar to display at the top of the scaffold.

final

backgroundColor → Color

The color of the Material widget that underlies the entire Scaffold. \[...\]

final

body → Widget

The primary content of the scaffold. \[...\]

final

bottomNavigationBar → Widget

A bottom navigation bar to display at the bottom of the scaffold. \[...\]

final

bottomSheet → Widget

The persistent bottom sheet to display. \[...\]

final

drawer → Widget

A panel displayed to the side of the body, often hidden on mobile devices. Swipes in from either left-to-right (TextDirection.ltr) or right-to-left (TextDirection.rtl) \[...\]

final

drawerDragStartBehavior → DragStartBehavior

Determines the way that drag start behavior is handled. \[...\]

final

drawerEdgeDragWidth → double

The width of the area within which a horizontal swipe will open the drawer. \[...\]

final

drawerEnableOpenDragGesture → bool

Determines if the Scaffold.drawer can be opened with a drag gesture. \[...\]

final

drawerScrimColor → Color

The color to use for the scrim that obscures primary content while a drawer is open. \[...\]

final

endDrawer → Widget

A panel displayed to the side of the body, often hidden on mobile devices. Swipes in from right-to-left (TextDirection.ltr) or left-to-right (TextDirection.rtl) \[...\]

final

endDrawerEnableOpenDragGesture → bool

Determines if the Scaffold.endDrawer can be opened with a drag gesture. \[...\]

final

extendBody → bool

If true, and bottomNavigationBar or persistentFooterButtons is specified, then the body extends to the bottom of the Scaffold, instead of only extending to the top of the bottomNavigationBar or the persistentFooterButtons. \[...\]

final

extendBodyBehindAppBar → bool

If true, and an appBar is specified, then the height of the body is extended to include the height of the app bar and the top of the body is aligned with the top of the app bar. \[...\]

final

floatingActionButton → Widget

A button displayed floating above body, in the bottom right corner. \[...\]

final

floatingActionButtonAnimator → FloatingActionButtonAnimator

Animator to move the floatingActionButton to a new floatingActionButtonLocation. \[...\]

final

floatingActionButtonLocation → FloatingActionButtonLocation

Responsible for determining where the floatingActionButton should go. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

persistentFooterButtons → List<Widget>

A set of buttons that are displayed at the bottom of the scaffold. \[...\]

final

primary → bool

Whether this scaffold is being displayed at the top of the screen. \[...\]

final

resizeToAvoidBottomInset → bool

If true the body and the scaffold's floating widgets should size themselves to avoid the onscreen keyboard whose height is defined by the ambient MediaQuery's MediaQueryData.viewInsets `bottom` property. \[...\]

final

resizeToAvoidBottomPadding → bool

This flag is deprecated, please use resizeToAvoidBottomInset instead. \[...\]

@Deprecated('Use resizeToAvoidBottomInset to specify if the body should resize when the keyboard appears. ' 'This feature was deprecated after v1.1.9.'), final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

createElement() → StatefulElement

Creates a StatefulElement to manage this widget's location in the tree. \[...\]

inherited

createState() → ScaffoldState

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

## Static Methods ##

geometryOf(BuildContext context) → ValueListenable<ScaffoldGeometry>

Returns a ValueListenable for the ScaffoldGeometry for the closest Scaffold ancestor of the given context. \[...\]

hasDrawer(BuildContext context, \{bool registerForUpdates: true\}) → bool

Whether the Scaffold that most tightly encloses the given context has a drawer. \[...\]

of(BuildContext context, \{bool nullOk: false\}) → ScaffoldState

The state from the closest instance of this class that encloses the given context. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/scaffold.dart#L1021
[The Scaffold has a white background with a blue AppBar at the top. A blue FloatingActionButton is positioned at the bottom right corner of the Scaffold.]: https://flutter.github.io/assets-for-api-docs/assets/material/scaffold.png
[scaffold_background_color.png]: https://flutter.github.io/assets-for-api-docs/assets/material/scaffold_background_color.png
[scaffold_bottom_app_bar.png]: https://flutter.github.io/assets-for-api-docs/assets/material/scaffold_bottom_app_bar.png
[material.io_design_layout_responsive-layout-grid.html]: https://material.io/design/layout/responsive-layout-grid.html
[Add a Drawer to a screen]: https://flutter.dev/docs/cookbook/design/drawer
[Display a snackbar]: https://flutter.dev/docs/cookbook/design/snackbars
[Scaffold Sample Apps]: https://flutter.dev/docs/catalog/samples/Scaffold