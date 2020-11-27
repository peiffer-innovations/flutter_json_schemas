# FontFeature class Null safety #

A feature tag and value that affect the selection of glyphs in a font.

## Constructors ##

FontFeature(String feature, \[int value = 1\])

Creates a FontFeature object, which can be added to a TextStyle to change how the engine selects glyphs when rendering text. \[...\]

const

FontFeature.disable(String feature)

Create a FontFeature object that disables the feature with the given tag.

const

FontFeature.enable(String feature)

Create a FontFeature object that enables the feature with the given tag.

const

FontFeature.oldstyleFigures()

Use oldstyle figures. \[...\]

const

FontFeature.proportionalFigures()

Use proportional (varying width) figures. \[...\]

const

FontFeature.randomize()

Randomize the alternate forms used in text. \[...\]

const

FontFeature.slashedZero()

Use the slashed zero. \[...\]

const

FontFeature.stylisticSet(int value)

Select a stylistic set. \[...\]

factory

FontFeature.tabularFigures()

Use tabular (monospace) figures. \[...\]

const

## Properties ##

feature → String

The tag that identifies the effect of this feature. Must consist of 4 ASCII characters (typically lowercase letters). \[...\]

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

value → int

The value assigned to this feature. \[...\]

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

override