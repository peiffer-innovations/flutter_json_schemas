# FontWeight class Null safety #

The thickness of the glyphs used to draw the text

## Properties ##

hashCode → int

The hash code for this object. \[...\]

read-only, inherited

index → int

The encoded integer value of this font weight.

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

## Static Methods ##

lerp(FontWeight? a, FontWeight? b, double t) → FontWeight?

Linearly interpolates between two font weights. \[...\]

## Constants ##

bold → const FontWeight

A commonly used font weight that is heavier than normal.

`w700`

normal → const FontWeight

The default font weight.

`w400`

values → const List<FontWeight>

A list of all the font weights.

`const <FontWeight>[w100, w200, w300, w400, w500, w600, w700, w800, w900]`

w100 → const FontWeight

Thin, the least thick

`const FontWeight._(0)`

w200 → const FontWeight

Extra-light

`const FontWeight._(1)`

w300 → const FontWeight

Light

`const FontWeight._(2)`

w400 → const FontWeight

Normal / regular / plain

`const FontWeight._(3)`

w500 → const FontWeight

Medium

`const FontWeight._(4)`

w600 → const FontWeight

Semi-bold

`const FontWeight._(5)`

w700 → const FontWeight

Bold

`const FontWeight._(6)`

w800 → const FontWeight

Extra-bold

`const FontWeight._(7)`

w900 → const FontWeight

Black, the most thick

`const FontWeight._(8)`