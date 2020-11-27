[*description*][description]

# TextTheme class #

Material design text theme.

Definitions for the various typographical styles found in Material Design (e.g., button, caption). Rather than creating a TextTheme directly, you can obtain an instance as Typography.black or Typography.white.

To obtain the current text theme, call Theme.of with the current BuildContext and read the ThemeData.textTheme property.

The names of the TextTheme properties match this table from the [Material Design spec][] with two exceptions: the styles called H1-H6 in the spec are headline1-headline6 in the API, and body1,body2 are called bodyText1 and bodyText2.

![mio-design_2Fassets_2F1W8kyGVruuG_O8psvyiOaCf1lLFIMzB-N_2Ftypesystem-typescale.png][]

## Migrating from the 2014 names ##

The Material Design typography scheme was significantly changed in the current (2018) version of the specification ([https://material.io/design/typography][https_material.io_design_typography]).

The 2018 spec has thirteen text styles:

    NAME         SIZE  WEIGHT  SPACING
    headline1    96.0  light   -1.5
    headline2    60.0  light   -0.5
    headline3    48.0  regular  0.0
    headline4    34.0  regular  0.25
    headline5    24.0  regular  0.0
    headline6    20.0  medium   0.15
    subtitle1    16.0  regular  0.15
    subtitle2    14.0  medium   0.1
    body1        16.0  regular  0.5   (bodyText1)
    body2        14.0  regular  0.25  (bodyText2)
    button       14.0  medium   1.25
    caption      12.0  regular  0.4
    overline     10.0  regular  1.5

...where "light" is `FontWeight.w300`, "regular" is `FontWeight.w400` and "medium" is `FontWeight.w500`.

The TextTheme API was originally based on the original material (2014) design spec, which used different text style names. For backwards compatibility's sake, this API continues to expose the old names. The table below should help with understanding the mapping of the API's old names and the new names (those in terms of the 2018 material specification).

Each of the TextTheme text styles corresponds to one of the styles from 2018 spec. By default, the font sizes, font weights and letter spacings have not changed from their original, 2014, values.

    NAME       SIZE   WEIGHT   SPACING  2018 NAME
    display4   112.0  thin     0.0      headline1
    display3   56.0   normal   0.0      headline2
    display2   45.0   normal   0.0      headline3
    display1   34.0   normal   0.0      headline4
    headline   24.0   normal   0.0      headline5
    title      20.0   medium   0.0      headline6
    subhead    16.0   normal   0.0      subtitle1
    body2      14.0   medium   0.0      body1 (bodyText1)
    body1      14.0   normal   0.0      body2 (bodyText2)
    caption    12.0   normal   0.0      caption
    button     14.0   medium   0.0      button
    subtitle   14.0   medium   0.0      subtitle2
    overline   10.0   normal   0.0      overline

Where "thin" is `FontWeight.w100`, "normal" is `FontWeight.w400` and "medium" is `FontWeight.w500`. Letter spacing for all of the original text styles was 0.0.

The old names are deprecated in this API.

Since the names `body1` and `body2` are used in both specifications but with different meanings, the API uses the terms `bodyText1` and `bodyText2` for the new API.

To configure a Theme for the new sizes, weights, and letter spacings, initialize its ThemeData.typography value using Typography.material2018.

See also:

 *  Typography, the class that generates TextThemes appropriate for a platform.
 *  Theme, for other aspects of a material design application that can be globally adjusted, such as the color scheme.
 *  [material.io/design/typography/][material.io_design_typography]

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

TextTheme(\{TextStyle headline1, TextStyle headline2, TextStyle headline3, TextStyle headline4, TextStyle headline5, TextStyle headline6, TextStyle subtitle1, TextStyle subtitle2, TextStyle bodyText1, TextStyle bodyText2, TextStyle caption, TextStyle button, TextStyle overline, @Deprecated('This is the term used in the 2014 version of material design. The modern term is headline1. ' 'This feature was deprecated after v1.13.8.') TextStyle display4, @Deprecated('This is the term used in the 2014 version of material design. The modern term is headline2. ' 'This feature was deprecated after v1.13.8.') TextStyle display3, @Deprecated('This is the term used in the 2014 version of material design. The modern term is headline3. ' 'This feature was deprecated after v1.13.8.') TextStyle display2, @Deprecated('This is the term used in the 2014 version of material design. The modern term is headline4. ' 'This feature was deprecated after v1.13.8.') TextStyle display1, @Deprecated('This is the term used in the 2014 version of material design. The modern term is headline5. ' 'This feature was deprecated after v1.13.8.') TextStyle headline, @Deprecated('This is the term used in the 2014 version of material design. The modern term is headline6. ' 'This feature was deprecated after v1.13.8.') TextStyle title, @Deprecated('This is the term used in the 2014 version of material design. The modern term is subtitle1. ' 'This feature was deprecated after v1.13.8.') TextStyle subhead, @Deprecated('This is the term used in the 2014 version of material design. The modern term is subtitle2. ' 'This feature was deprecated after v1.13.8.') TextStyle subtitle, @Deprecated('This is the term used in the 2014 version of material design. The modern term is bodyText1. ' 'This feature was deprecated after v1.13.8.') TextStyle body2, @Deprecated('This is the term used in the 2014 version of material design. The modern term is bodyText2. ' 'This feature was deprecated after v1.13.8.') TextStyle body1\})

Creates a text theme that uses the given values. \[...\]

const

## Properties ##

body1 → TextStyle

Used for the default text style for Material. \[...\]

@Deprecated('This is the term used in the 2014 version of material design. The modern term is bodyText2. ' 'This feature was deprecated after v1.13.8.'), read-only

body2 → TextStyle

Used for emphasizing text that would otherwise be body1. \[...\]

@Deprecated('This is the term used in the 2014 version of material design. The modern term is bodyText1. ' 'This feature was deprecated after v1.13.8.'), read-only

bodyText1 → TextStyle

Used for emphasizing text that would otherwise be bodyText2.

final

bodyText2 → TextStyle

The default text style for Material.

final

button → TextStyle

Used for text on ElevatedButton, TextButton and OutlinedButton.

final

caption → TextStyle

Used for auxiliary text associated with images.

final

display1 → TextStyle

Large text. \[...\]

@Deprecated('This is the term used in the 2014 version of material design. The modern term is headline4. ' 'This feature was deprecated after v1.13.8.'), read-only

display2 → TextStyle

Very large text. \[...\]

@Deprecated('This is the term used in the 2014 version of material design. The modern term is headline3. ' 'This feature was deprecated after v1.13.8.'), read-only

display3 → TextStyle

Very, very large text. \[...\]

@Deprecated('This is the term used in the 2014 version of material design. The modern term is headline2. ' 'This feature was deprecated after v1.13.8.'), read-only

display4 → TextStyle

Extremely large text. \[...\]

@Deprecated('This is the term used in the 2014 version of material design. The modern term is headline1. ' 'This feature was deprecated after v1.13.8.'), read-only

hashCode → int

The hash code for this object. \[...\]

read-only, override

headline → TextStyle

Used for large text in dialogs. \[...\]

@Deprecated('This is the term used in the 2014 version of material design. The modern term is headline5. ' 'This feature was deprecated after v1.13.8.'), read-only

headline1 → TextStyle

Extremely large text.

final

headline2 → TextStyle

Very, very large text. \[...\]

final

headline3 → TextStyle

Very large text.

final

headline4 → TextStyle

Large text.

final

headline5 → TextStyle

Used for large text in dialogs (e.g., the month and year in the dialog shown by showDatePicker).

final

headline6 → TextStyle

Used for the primary text in app bars and dialogs (e.g., AppBar.title and AlertDialog.title).

final

overline → TextStyle

The smallest style. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

subhead → TextStyle

Used for the primary text in lists (e.g., ListTile.title). \[...\]

@Deprecated('This is the term used in the 2014 version of material design. The modern term is subtitle1. ' 'This feature was deprecated after v1.13.8.'), read-only

subtitle → TextStyle

For medium emphasis text that's a little smaller than subhead. \[...\]

@Deprecated('This is the term used in the 2014 version of material design. The modern term is subtitle2. ' 'This feature was deprecated after v1.13.8.'), read-only

subtitle1 → TextStyle

Used for the primary text in lists (e.g., ListTile.title).

final

subtitle2 → TextStyle

For medium emphasis text that's a little smaller than subtitle1.

final

title → TextStyle

Used for the primary text in app bars and dialogs. \[...\]

@Deprecated('This is the term used in the 2014 version of material design. The modern term is headline6. ' 'This feature was deprecated after v1.13.8.'), read-only

## Methods ##

apply(\{String fontFamily, double fontSizeFactor: 1.0, double fontSizeDelta: 0.0, Color displayColor, Color bodyColor, TextDecoration decoration, Color decorationColor, TextDecorationStyle decorationStyle\}) → TextTheme

Creates a copy of this text theme but with the given field replaced in each of the individual text styles. \[...\]

copyWith(\{TextStyle headline1, TextStyle headline2, TextStyle headline3, TextStyle headline4, TextStyle headline5, TextStyle headline6, TextStyle subtitle1, TextStyle subtitle2, TextStyle bodyText1, TextStyle bodyText2, TextStyle caption, TextStyle button, TextStyle overline, TextStyle display4, TextStyle display3, TextStyle display2, TextStyle display1, TextStyle headline, TextStyle title, TextStyle subhead, TextStyle subtitle, TextStyle body2, TextStyle body1\}) → TextTheme

Creates a copy of this text theme but with the given fields replaced with the new values. \[...\]

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

override

merge(TextTheme other) → TextTheme

Creates a new TextTheme where each text style from this object has been merged with the matching text style from the `other` object. \[...\]

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

toDiagnosticsNode(\{String name, DiagnosticsTreeStyle style\}) → DiagnosticsNode

Returns a debug representation of the object that is used by debugging tools and by DiagnosticsNode.toStringDeep. \[...\]

inherited

toString(\{DiagnosticLevel minLevel: DiagnosticLevel.info\}) → String

Returns a string representation of this object.

inherited

toStringShort() → String

A brief description of this object, usually just the runtimeType and the hashCode. \[...\]

inherited

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

override

## Static Methods ##

lerp(TextTheme a, TextTheme b, double t) → TextTheme

Linearly interpolate between two text themes. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/text_theme.dart#L104
[Material Design spec]: https://material.io/design/typography/the-type-system.html#type-scale
[mio-design_2Fassets_2F1W8kyGVruuG_O8psvyiOaCf1lLFIMzB-N_2Ftypesystem-typescale.png]: https://storage.googleapis.com/spec-host-backup/mio-design%2Fassets%2F1W8kyGVruuG_O8psvyiOaCf1lLFIMzB-N%2Ftypesystem-typescale.png
[https_material.io_design_typography]: https://material.io/design/typography
[material.io_design_typography]: https://material.io/design/typography/