[*description*][description]

# IconData class #

A description of an icon fulfilled by a font glyph.

See Icons for a number of predefined icons available for material design applications.

Annotations

 *  @immutable

## Constructors ##

IconData(int codePoint, \{String fontFamily, String fontPackage, bool matchTextDirection: false\})

Creates icon data. \[...\]

const

## Properties ##

codePoint → int

The Unicode code point at which this icon is stored in the icon font.

final

fontFamily → String

The font family from which the glyph for the codePoint will be selected.

final

fontPackage → String

The name of the package from which the font family is included. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

matchTextDirection → bool

Whether this icon should be automatically mirrored in right-to-left environments. \[...\]

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

override


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/icon_data.dart#L16