[*description*][description]

# CrossFadeState enum #

Specifies which of two children to show. See AnimatedCrossFade.

The child that is shown will fade in, while the other will fade out.

## Constants ##

showFirst → const CrossFadeState

Show the first child (AnimatedCrossFade.firstChild) and hide the second (AnimatedCrossFade.secondChild\]).

`const CrossFadeState(0)`

showSecond → const CrossFadeState

Show the second child (AnimatedCrossFade.secondChild) and hide the first (AnimatedCrossFade.firstChild).

`const CrossFadeState(1)`

values → const List<CrossFadeState>

A constant List of the values in this enum, in order of their declaration.

`const List<CrossFadeState>`

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/animated_cross_fade.dart#L21