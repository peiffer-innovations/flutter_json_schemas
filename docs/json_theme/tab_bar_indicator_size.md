[*description*][description]

# TabBarIndicatorSize enum #

Defines how the bounds of the selected tab indicator are computed.

See also:

 *  TabBar, which displays a row of tabs.
 *  TabBarView, which displays a widget for the currently selected tab.
 *  TabBar.indicator, which defines the appearance of the selected tab indicator relative to the tab's bounds.

## Constants ##

label → const TabBarIndicatorSize

The tab's bounds are only as wide as the (centered) tab widget itself.

This value is used to align the tab's label, typically a Tab widget's text or icon, with the selected tab indicator.

`const TabBarIndicatorSize(1)`

tab → const TabBarIndicatorSize

The tab indicator's bounds are as wide as the space occupied by the tab in the tab bar: from the right edge of the previous tab to the left edge of the next tab.

`const TabBarIndicatorSize(0)`

values → const List<TabBarIndicatorSize>

A constant List of the values in this enum, in order of their declaration.

`const List<TabBarIndicatorSize>`

## Properties ##

hashCode → int

The hash code for this object. \[...\]

read-only, inherited

index → int

The integer index of this enum.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

toString() → String

Returns a string representation of this object.

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/tabs.dart#L37