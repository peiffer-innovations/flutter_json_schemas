# FilterQuality enum Null safety #

Quality levels for image filters.

See Paint.filterQuality.

## Constants ##

high → const FilterQuality

Best possible quality filtering, albeit also the slowest.

Typically this implies bicubic interpolation or better.

`const FilterQuality(3)`

low → const FilterQuality

Better quality than none, faster than medium.

Typically this implies bilinear interpolation.

`const FilterQuality(1)`

medium → const FilterQuality

Better quality than low, faster than high.

Typically this implies a combination of bilinear interpolation and pyramidal parametric pre-filtering (mipmaps).

`const FilterQuality(2)`

none → const FilterQuality

Fastest possible filtering, albeit also the lowest quality.

Typically this implies nearest-neighbor filtering.

`const FilterQuality(0)`

values → const List<FilterQuality>

A constant List of the values in this enum, in order of their declaration.

`const List<FilterQuality>`

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