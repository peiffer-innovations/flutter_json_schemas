[*description*][description]

# Typography class #

The color and geometry TextThemes for Material apps.

The text themes provided by the overall Theme, like ThemeData.textTheme, are based on the current locale's MaterialLocalizations.scriptCategory and are created by merging a color text theme, black or white and a geometry text theme, one of englishLike, dense, or tall, depending on the locale.

To lookup a localized text theme use `Theme.of(context).textTheme` or `Theme.of(context).primaryTextTheme` or `Theme.of(context).accentTextTheme`.

The color text themes are blackMountainView, whiteMountainView, blackCupertino, and whiteCupertino. The Mountain View theme TextStyles are based on the Roboto fonts as used on Android. The Cupertino themes are based on the [San Francisco font][] fonts as used by Apple on iOS.

Two sets of geometry themes are provided: 2014 and 2018. The 2014 themes correspond to the original version of the Material Design spec and are the defaults. The 2018 themes correspond the second iteration of the specification and feature different font sizes, font weights, and letter spacing values.

By default, ThemeData.typography is `Typography.material2014(platform: platform)` which uses englishLike2014, dense2014 and tall2014. To use the 2018 text theme geometries, specify a value using the material2018 constructor:

    typography: Typography.material2018(platform: platform)

See also:

 *  ThemeData.typography, which can be used to configure the text themes used to create ThemeData.textTheme, ThemeData.primaryTextTheme, ThemeData.accentTextTheme.
 *  [material.io/design/typography/][material.io_design_typography]

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

Typography(\{TargetPlatform platform, TextTheme black, TextTheme white, TextTheme englishLike, TextTheme dense, TextTheme tall\})

Creates a typography instance. \[...\]

factory

Typography.material2014(\{TargetPlatform platform: TargetPlatform.android, TextTheme black, TextTheme white, TextTheme englishLike, TextTheme dense, TextTheme tall\})

Creates a typography instance using material design's 2014 defaults. \[...\]

factory

Typography.material2018(\{TargetPlatform platform: TargetPlatform.android, TextTheme black, TextTheme white, TextTheme englishLike, TextTheme dense, TextTheme tall\})

Creates a typography instance using material design's 2018 defaults. \[...\]

factory

## Properties ##

black → TextTheme

A material design text theme with dark glyphs. \[...\]

final

dense → TextTheme

Defines text geometry for dense scripts, such as Chinese, Japanese and Korean. \[...\]

final

englishLike → TextTheme

Defines text geometry for ScriptCategory.englishLike scripts, such as English, French, Russian, etc. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

tall → TextTheme

Defines text geometry for tall scripts, such as Farsi, Hindi, and Thai. \[...\]

final

white → TextTheme

A material design text theme with light glyphs. \[...\]

final

## Methods ##

copyWith(\{TextTheme black, TextTheme white, TextTheme englishLike, TextTheme dense, TextTheme tall\}) → Typography

Creates a copy of this Typography with the given fields replaced by the non-null parameter values.

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

override

geometryThemeFor(ScriptCategory category) → TextTheme

Returns one of englishLike, dense, or tall.

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

lerp(Typography a, Typography b, double t) → Typography

Linearly interpolate between two Typography objects. \[...\]

## Constants ##

blackCupertino → const TextTheme

A material design text theme with dark glyphs based on San Francisco. \[...\]

`TextTheme(headline1: TextStyle(debugLabel: 'blackCupertino headline1', fontFamily: '.SF UI Display', inherit: true, color: Colors.black54, decoration: TextDecoration.none), headline2: …`

blackHelsinki → const TextTheme

A material design text theme with dark glyphs based on Roboto, with fallback fonts that are likely (but not guaranteed) to be installed on Linux. \[...\]

`TextTheme(headline1: TextStyle(debugLabel: 'blackHelsinki headline1', fontFamily: 'Roboto', fontFamilyFallback: _helsinkiFontFallbacks, inherit: true, color: Colors.black54, decoration…`

blackMountainView → const TextTheme

A material design text theme with dark glyphs based on Roboto. \[...\]

`TextTheme(headline1: TextStyle(debugLabel: 'blackMountainView headline1', fontFamily: 'Roboto', inherit: true, color: Colors.black54, decoration: TextDecoration.none), headline2: TextS…`

blackRedmond → const TextTheme

A material design text theme with dark glyphs based on Segoe UI. \[...\]

`TextTheme(headline1: TextStyle(debugLabel: 'blackRedmond headline1', fontFamily: 'Segoe UI', inherit: true, color: Colors.black54, decoration: TextDecoration.none), headline2: TextStyl…`

dense2014 → const TextTheme

Defines text geometry for dense scripts, such as Chinese, Japanese and Korean.

`TextTheme(headline1: TextStyle(debugLabel: 'dense display4 2014', inherit: false, fontSize: 112.0, fontWeight: FontWeight.w100, textBaseline: TextBaseline.ideographic), headline2: TextStyle(de…`

dense2018 → const TextTheme

Defines text geometry for dense scripts, such as Chinese, Japanese and Korean. \[...\]

`TextTheme(headline1: TextStyle(debugLabel: 'dense headline1 2018', fontSize: 96.0, fontWeight: FontWeight.w100, textBaseline: TextBaseline.ideographic), headline2: TextStyle(debugLabel: 'd…`

englishLike2014 → const TextTheme

Defines text geometry for ScriptCategory.englishLike scripts, such as English, French, Russian, etc.

`TextTheme(headline1: TextStyle(debugLabel: 'englishLike display4 2014', inherit: false, fontSize: 112.0, fontWeight: FontWeight.w100, textBaseline: TextBaseline.alphabetic), headline2: TextSty…`

englishLike2018 → const TextTheme

Defines text geometry for ScriptCategory.englishLike scripts, such as English, French, Russian, etc. \[...\]

`TextTheme(headline1: TextStyle(debugLabel: 'englishLike headline1 2018', fontSize: 96.0, fontWeight: FontWeight.w300, textBaseline: TextBaseline.alphabetic, letterSpacing: -1.5), headline2: Te…`

tall2014 → const TextTheme

Defines text geometry for tall scripts, such as Farsi, Hindi, and Thai.

`TextTheme(headline1: TextStyle(debugLabel: 'tall display4 2014', inherit: false, fontSize: 112.0, fontWeight: FontWeight.w400, textBaseline: TextBaseline.alphabetic), headline2: TextStyle(debu…`

tall2018 → const TextTheme

Defines text geometry for tall scripts, such as Farsi, Hindi, and Thai. \[...\]

`TextTheme(headline1: TextStyle(debugLabel: 'tall headline1 2018', fontSize: 96.0, fontWeight: FontWeight.w400, textBaseline: TextBaseline.alphabetic), headline2: TextStyle(debugLabel: 'tal…`

whiteCupertino → const TextTheme

A material design text theme with light glyphs based on San Francisco. \[...\]

`TextTheme(headline1: TextStyle(debugLabel: 'whiteCupertino headline1', fontFamily: '.SF UI Display', inherit: true, color: Colors.white70, decoration: TextDecoration.none), headline2: …`

whiteHelsinki → const TextTheme

A material design text theme with light glyphs based on Roboto, with fallbacks of DejaVu Sans, Liberation Sans and Arial. \[...\]

`TextTheme(headline1: TextStyle(debugLabel: 'whiteHelsinki headline1', fontFamily: 'Roboto', fontFamilyFallback: _helsinkiFontFallbacks, inherit: true, color: Colors.white70, decoration…`

whiteMountainView → const TextTheme

A material design text theme with light glyphs based on Roboto. \[...\]

`TextTheme(headline1: TextStyle(debugLabel: 'whiteMountainView headline1', fontFamily: 'Roboto', inherit: true, color: Colors.white70, decoration: TextDecoration.none), headline2: TextS…`

whiteRedmond → const TextTheme

A material design text theme with light glyphs based on Segoe UI. \[...\]

`TextTheme(headline1: TextStyle(debugLabel: 'whiteRedmond headline1', fontFamily: 'Segoe UI', inherit: true, color: Colors.white70, decoration: TextDecoration.none), headline2: TextStyl…`


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/typography.dart#L87
[San Francisco font]: https://developer.apple.com/ios/human-interface-guidelines/visual-design/typography/
[material.io_design_typography]: https://material.io/design/typography/