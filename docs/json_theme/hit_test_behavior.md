[*description*][description]

# HitTestBehavior enum Null safety #

How to behave during hit tests.

## Constants ##

deferToChild → const HitTestBehavior

Targets that defer to their children receive events within their bounds only if one of their children is hit by the hit test.

`const HitTestBehavior(0)`

opaque → const HitTestBehavior

Opaque targets can be hit by hit tests, causing them to both receive events within their bounds and prevent targets visually behind them from also receiving events.

`const HitTestBehavior(1)`

translucent → const HitTestBehavior

Translucent targets both receive events within their bounds and permit targets visually behind them to also receive events.

`const HitTestBehavior(2)`

values → const List<HitTestBehavior>

A constant List of the values in this enum, in order of their declaration.

`const List<HitTestBehavior>`

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/rendering/proxy_box.dart#L136