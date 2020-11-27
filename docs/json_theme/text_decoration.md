# TextDecoration class Null safety #

A linear decoration to draw near the text.

## Constructors ##

TextDecoration.combine(List<TextDecoration> decorations)

Creates a decoration that paints the union of all the given decorations.

factory

## Properties ##

hashCode → int

The hash code for this object. \[...\]

read-only, override

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

contains(TextDecoration other) → bool

Whether this decoration will paint at least as much decoration as the given decoration.

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

toString() → String

Returns a string representation of this object.

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

override

## Constants ##

lineThrough → const TextDecoration

Draw a line through each line of text

`const TextDecoration._(0x4)`

none → const TextDecoration

Do not draw a decoration

`const TextDecoration._(0x0)`

overline → const TextDecoration

Draw a line above each line of text

`const TextDecoration._(0x2)`

underline → const TextDecoration

Draw a line underneath each line of text

`const TextDecoration._(0x1)`