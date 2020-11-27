[*description*][description]

# DragStartBehavior enum Null safety #

Configuration of offset passed to DragStartDetails.

The settings determines when a drag formally starts when the user initiates a drag.

See also:

 *  DragGestureRecognizer.dragStartBehavior, which gives an example for the different behaviors.

## Constants ##

down → const DragStartBehavior

Set the initial offset, at the position where the first down event was detected.

`const DragStartBehavior(0)`

start → const DragStartBehavior

Set the initial position at the position where the drag start event was detected.

`const DragStartBehavior(1)`

values → const List<DragStartBehavior>

A constant List of the values in this enum, in order of their declaration.

`const List<DragStartBehavior>`

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/gestures/recognizer.dart#L37