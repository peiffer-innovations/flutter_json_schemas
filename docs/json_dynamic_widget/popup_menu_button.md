[*description*][description]

# PopupMenuButton<T> class #

Displays a menu when pressed and calls onSelected when the menu is dismissed because an item was selected. The value passed to onSelected is the value of the selected menu item.

One of child or icon may be provided, but not both. If icon is provided, then PopupMenuButton behaves like an IconButton.

If both are null, then a standard overflow icon is created (depending on the platform).

 *link* 

Sample

This example shows a menu with four items, selecting between an enum's values and setting a `_selection` field based on the selection.

*assignment*

    // This is the type used by the popup menu below.
    enum WhyFarther { harder, smarter, selfStarter, tradingCharter }
    
    // This menu button widget updates a _selection field (of type WhyFarther,
    // not shown here).
    PopupMenuButton<WhyFarther>(
      onSelected: (WhyFarther result) { setState(() { _selection = result; }); },
      itemBuilder: (BuildContext context) => <PopupMenuEntry<WhyFarther>>[
        const PopupMenuItem<WhyFarther>(
          value: WhyFarther.harder,
          child: Text('Working a lot harder'),
        ),
        const PopupMenuItem<WhyFarther>(
          value: WhyFarther.smarter,
          child: Text('Being a lot smarter'),
        ),
        const PopupMenuItem<WhyFarther>(
          value: WhyFarther.selfStarter,
          child: Text('Being a self-starter'),
        ),
        const PopupMenuItem<WhyFarther>(
          value: WhyFarther.tradingCharter,
          child: Text('Placed in charge of trading charter'),
        ),
      ],
    )

See also:

 *  PopupMenuItem, a popup menu entry for a single value.
 *  PopupMenuDivider, a popup menu entry that is just a horizontal line.
 *  CheckedPopupMenuItem, a popup menu item with a checkmark.
 *  showMenu, a method to dynamically show a popup menu at a given location.

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatefulWidget
 *  PopupMenuButton

## Constructors ##

PopupMenuButton(\{Key key, @required PopupMenuItemBuilder<T> itemBuilder, T initialValue, PopupMenuItemSelected<T> onSelected, PopupMenuCanceled onCanceled, String tooltip, double elevation, EdgeInsetsGeometry padding: const EdgeInsets.all(8.0), Widget child, Widget icon, Offset offset: Offset.zero, bool enabled: true, ShapeBorder shape, Color color, bool captureInheritedThemes: true\})

Creates a button that shows a popup menu. \[...\]

const

## Properties ##

captureInheritedThemes → bool

If true (the default) then the menu will be wrapped with copies of the InheritedThemes, like Theme and PopupMenuTheme, which are defined above the BuildContext where the menu is shown.

final

child → Widget

If provided, child is the widget used for this button and the button will utilize an InkWell for taps.

final

color → Color

If provided, the background color used for the menu. \[...\]

final

elevation → double

The z-coordinate at which to place the menu when open. This controls the size of the shadow below the menu. \[...\]

final

enabled → bool

Whether this popup menu button is interactive. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

icon → Widget

If provided, the icon is used for this button and the button will behave like an IconButton.

final

initialValue → T

The value of the menu item, if any, that should be highlighted when the menu opens.

final

itemBuilder → PopupMenuItemBuilder<T>

Called when the button is pressed to create the items to show in the menu.

final

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

offset → Offset

The offset applied to the Popup Menu Button. \[...\]

final

onCanceled → PopupMenuCanceled

Called when the user dismisses the popup menu without selecting an item. \[...\]

final

onSelected → PopupMenuItemSelected<T>

Called when the user selects a value from the popup menu created by this button. \[...\]

final

padding → EdgeInsetsGeometry

Matches IconButton's 8 dps padding by default. In some cases, notably where this button appears as the trailing element of a list item, it's useful to be able to set the padding to zero.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

shape → ShapeBorder

If provided, the shape used for the menu. \[...\]

final

tooltip → String

Text that describes the action that will occur when the button is pressed. \[...\]

final

## Methods ##

createElement() → StatefulElement

Creates a StatefulElement to manage this widget's location in the tree. \[...\]

inherited

createState() → PopupMenuButtonState<T>

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/popup_menu.dart#L960