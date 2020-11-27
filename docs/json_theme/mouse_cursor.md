[*description*][description]

# MouseCursor class Null safety #

An interface for mouse cursor definitions.

A mouse cursor is a graphical image on the screen that echoes the movement of a pointing device, such as a mouse or a stylus. A MouseCursor object defines a kind of mouse cursor, such as an arrow, a pointing hand, or an I-beam.

During the painting phase, MouseCursor objects are assigned to regions on the screen via annotations. Later during a device update (e.g. when a mouse moves), MouseTracker finds the *active cursor* of each mouse device, which is the front-most region associated with the position of each mouse cursor, or defaults to SystemMouseCursors.basic if no cursors are associated with the position. MouseTracker changes the cursor of the pointer if the new active cursor is different from the previous active cursor, whose effect is defined by the session created by createSession.

## Cursor classes ##

A SystemMouseCursor is a cursor that is natively supported by the platform that the program is running on. All supported system mouse cursors are enumerated in SystemMouseCursors.

## Using cursors ##

A MouseCursor object is used by being assigned to a MouseRegion or another widget that exposes the MouseRegion API, such as InkResponse.mouseCursor.

 *link* 

Sample

This sample creates a rectangular region that is wrapped by a MouseRegion with a system mouse cursor. The mouse pointer becomes an I-beam when hovering over the region.

*assignment*

    Widget build(BuildContext context) {
      return Center(
        child: MouseRegion(
          cursor: SystemMouseCursors.text,
          child: Container(
            width: 200,
            height: 100,
            decoration: BoxDecoration(
              color: Colors.blue,
              border: Border.all(color: Colors.yellow),
            ),
          ),
        ),
      );
    }

Assigning regions with mouse cursors on platforms that do not support mouse cursors, or when there are no mice connected, will have no effect.

## Related classes ##

MouseCursorSession represents the duration when a pointing device displays a cursor, and defines the states and behaviors of the cursor. Every mouse cursor class usually has a corresponding MouseCursorSession class.

MouseTrackerCursorMixin is a mixin that adds the feature of changing cursors to BaseMouseTracker, which tracks the relationship between mouse devices and annotations. MouseTrackerCursorMixin is usually used as a part of MouseTracker.

Mixed in types

 *  Diagnosticable

Implementers

 *  MaterialStateMouseCursor
 *  SystemMouseCursor

Annotations

 *  @immutable

## Constructors ##

MouseCursor()

Abstract const constructor. This constructor enables subclasses to provide const constructors so that they can be used in const expressions.

const

## Properties ##

debugDescription → String

A very short description of the mouse cursor. \[...\]

read-only

hashCode → int

The hash code for this object. \[...\]

read-only, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

createSession(int device) → MouseCursorSession

Associate a pointing device to this cursor. \[...\]

@factory, @protected

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

@mustCallSuper, @protected, inherited

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

toDiagnosticsNode(\{String? name, DiagnosticsTreeStyle? style\}) → DiagnosticsNode

Returns a debug representation of the object that is used by debugging tools and by DiagnosticsNode.toStringDeep. \[...\]

inherited

toString(\{DiagnosticLevel minLevel: DiagnosticLevel.info\}) → String

Returns a string representation of this object.

override

toStringShort() → String

A brief description of this object, usually just the runtimeType and the hashCode. \[...\]

inherited

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

inherited

## Constants ##

defer → const MouseCursor

A special class that indicates that the region with this cursor defers the choice of cursor to the next region behind it. \[...\]

`_DeferringMouseCursor._()`

uncontrolled → const MouseCursor

A special value that doesn't change cursor by itself, but make a region that blocks other regions behind it from changing the cursor. \[...\]

`_NoopMouseCursor._()`


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/rendering/mouse_cursor.dart#L201