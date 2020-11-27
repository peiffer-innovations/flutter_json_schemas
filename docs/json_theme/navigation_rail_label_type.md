[*description*][description]

# NavigationRailLabelType enum #

Defines the behavior of the labels of a NavigationRail.

See also:

 *  NavigationRail

## Constants ##

all → const NavigationRailLabelType

All NavigationRailDestinations will show their label.

`const NavigationRailLabelType(2)`

none → const NavigationRailLabelType

Only the NavigationRailDestinations are shown.

`const NavigationRailLabelType(0)`

selected → const NavigationRailLabelType

Only the selected NavigationRailDestination will show its label.

The label will animate in and out as new NavigationRailDestinations are selected.

`const NavigationRailLabelType(1)`

values → const List<NavigationRailLabelType>

A constant List of the values in this enum, in order of their declaration.

`const List<NavigationRailLabelType>`

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/navigation_rail.dart#L787