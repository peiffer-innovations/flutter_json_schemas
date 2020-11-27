[*description*][description]

# ScrollViewKeyboardDismissBehavior enum #

A representation of how a ScrollView should dismiss the on-screen keyboard.

## Constants ##

manual → const ScrollViewKeyboardDismissBehavior

`manual` means there is no automatic dismissal of the on-screen keyboard. It is up to the client to dismiss the keyboard.

`const ScrollViewKeyboardDismissBehavior(0)`

onDrag → const ScrollViewKeyboardDismissBehavior

`onDrag` means that the ScrollView will dismiss an on-screen keyboard when a drag begins.

`const ScrollViewKeyboardDismissBehavior(1)`

values → const List<ScrollViewKeyboardDismissBehavior>

A constant List of the values in this enum, in order of their declaration.

`const List<ScrollViewKeyboardDismissBehavior>`

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/scroll_view.dart#L32