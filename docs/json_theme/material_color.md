[*description*][description]

# MaterialColor class #

Defines a single color as well a color swatch with ten shades of the color.

The color's shades are referred to by index. The greater the index, the darker the color. There are 10 valid indices: 50, 100, 200, ..., 900. The value of this color should the same the value of index 500 and shade500.

See also:

 *  Colors, which defines all of the standard material colors.

Inheritance

 *  Object
 *  Color
 *  ColorSwatch<int>
 *  MaterialColor

## Constructors ##

MaterialColor(int primary, Map<int, Color> swatch)

Creates a color swatch with a variety of shades. \[...\]

const

## Properties ##

alpha → int

The alpha channel of this color in an 8 bit value. \[...\]

read-only, inherited

blue → int

The blue channel of this color in an 8 bit value.

read-only, inherited

green → int

The green channel of this color in an 8 bit value.

read-only, inherited

hashCode → int

The hash code for this object. \[...\]

read-only, inherited

opacity → double

The alpha channel of this color as a double. \[...\]

read-only, inherited

red → int

The red channel of this color in an 8 bit value.

read-only, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

shade50 → Color

The lightest shade.

read-only

shade100 → Color

The second lightest shade.

read-only

shade200 → Color

The third lightest shade.

read-only

shade300 → Color

The fourth lightest shade.

read-only

shade400 → Color

The fifth lightest shade.

read-only

shade500 → Color

The default shade.

read-only

shade600 → Color

The fourth darkest shade.

read-only

shade700 → Color

The third darkest shade.

read-only

shade800 → Color

The second darkest shade.

read-only

shade900 → Color

The darkest shade.

read-only

value → int

A 32 bit value representing this color. \[...\]

final, inherited

## Methods ##

computeLuminance() → double

Returns a brightness value between 0 for darkest and 1 for lightest. \[...\]

inherited

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

toString() → String

Returns a string representation of this object.

inherited

withAlpha(int a) → Color

Returns a new color that matches this color with the alpha channel replaced with `a` (which ranges from 0 to 255). \[...\]

inherited

withBlue(int b) → Color

Returns a new color that matches this color with the blue channel replaced with `b` (which ranges from 0 to 255). \[...\]

inherited

withGreen(int g) → Color

Returns a new color that matches this color with the green channel replaced with `g` (which ranges from 0 to 255). \[...\]

inherited

withOpacity(double opacity) → Color

Returns a new color that matches this color with the alpha channel replaced with the given `opacity` (which ranges from 0.0 to 1.0). \[...\]

inherited

withRed(int r) → Color

Returns a new color that matches this color with the red channel replaced with `r` (which ranges from 0 to 255). \[...\]

inherited

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

inherited

operator \[\](int index) → Color

Returns an element of the swatch table.

inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/colors.dart#L20