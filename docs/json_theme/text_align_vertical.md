[*description*][description]

# TextAlignVertical class Null safety #

The vertical alignment of text within an input box.

A single y value that can range from -1.0 to 1.0. -1.0 aligns to the top of an input box so that the top of the first line of text fits within the box and its padding. 0.0 aligns to the center of the box. 1.0 aligns so that the bottom of the last line of text aligns with the bottom interior edge of the input box.

See also:

 *  TextField.textAlignVertical, which is passed on to the InputDecorator.
 *  CupertinoTextField.textAlignVertical, which behaves in the same way as the parameter in TextField.
 *  InputDecorator.textAlignVertical, which defines the alignment of prefix, input, and suffix within an InputDecorator.

## Constructors ##

TextAlignVertical(\{required double y\})

Creates a TextAlignVertical from any y value between -1.0 and 1.0.

const

## Properties ##

hashCode → int

The hash code for this object. \[...\]

read-only, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

y → double

A value ranging from -1.0 to 1.0 that defines the topmost and bottommost locations of the top and bottom of the input box.

final

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

## Constants ##

bottom → const TextAlignVertical

Aligns a TextField's input Text with the bottommost location within a TextField.

`TextAlignVertical(y: 1.0)`

center → const TextAlignVertical

Aligns a TextField's input Text to the center of the TextField.

`TextAlignVertical(y: 0.0)`

top → const TextAlignVertical

Aligns a TextField's input Text with the topmost location within a TextField's input box.

`TextAlignVertical(y: -1.0)`


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/painting/alignment.dart#L649