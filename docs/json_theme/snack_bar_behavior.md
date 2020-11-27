[*description*][description]

# SnackBarBehavior enum #

Defines where a SnackBar should appear within a Scaffold and how its location should be adjusted when the scaffold also includes a FloatingActionButton or a BottomNavigationBar.

## Constants ##

fixed → const SnackBarBehavior

Fixes the SnackBar at the bottom of the Scaffold.

The exception is that the SnackBar will be shown above a BottomNavigationBar. Additionally, the SnackBar will cause other non-fixed widgets inside Scaffold to be pushed above (for example, the FloatingActionButton).

`const SnackBarBehavior(0)`

floating → const SnackBarBehavior

This behavior will cause SnackBar to be shown above other widgets in the Scaffold. This includes being displayed above a BottomNavigationBar and a FloatingActionButton.

See [material.io/design/components/snackbars.html][material.io_design_components_snackbars.html] for more details.

`const SnackBarBehavior(1)`

values → const List<SnackBarBehavior>

A constant List of the values in this enum, in order of their declaration.

`const List<SnackBarBehavior>`

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/snack_bar_theme.dart#L17
[material.io_design_components_snackbars.html]: https://material.io/design/components/snackbars.html