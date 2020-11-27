# TextHeightBehavior class Null safety #

Defines how the paragraph will apply TextStyle.height to the ascent of the first line and descent of the last line.

Each boolean value represents whether the TextStyle.height modifier will be applied to the corresponding metric. By default, all properties are true, and TextStyle.height is applied as normal. When set to false, the font's default ascent will be used.

## Constructors ##

TextHeightBehavior(\{bool applyHeightToFirstAscent: true, bool applyHeightToLastDescent: true\})

Creates a new TextHeightBehavior object. \[...\]

const

TextHeightBehavior.fromEncoded(int encoded)

Creates a new TextHeightBehavior object from an encoded form. \[...\]

const

## Properties ##

applyHeightToFirstAscent → bool

Whether to apply the TextStyle.height modifier to the ascent of the first line in the paragraph. \[...\]

final

applyHeightToLastDescent → bool

Whether to apply the TextStyle.height modifier to the descent of the last line in the paragraph. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

encode() → int

Returns an encoded int representation of this object.

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