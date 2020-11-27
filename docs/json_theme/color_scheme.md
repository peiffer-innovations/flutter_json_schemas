[*description*][description]

# ColorScheme class #

A set of twelve colors based on the [Material spec][] that can be used to configure the color properties of most components.

The Theme has a color scheme, ThemeData.colorScheme, which is constructed with ColorScheme.fromSwatch.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

ColorScheme(\{@required Color primary, @required Color primaryVariant, @required Color secondary, @required Color secondaryVariant, @required Color surface, @required Color background, @required Color error, @required Color onPrimary, @required Color onSecondary, @required Color onSurface, @required Color onBackground, @required Color onError, @required Brightness brightness\})

Create a ColorScheme instance.

const

ColorScheme.dark(\{Color primary: const Color(0xffbb86fc), Color primaryVariant: const Color(0xff3700B3), Color secondary: const Color(0xff03dac6), Color secondaryVariant: const Color(0xff03dac6), Color surface: const Color(0xff121212), Color background: const Color(0xff121212), Color error: const Color(0xffcf6679), Color onPrimary: Colors.black, Color onSecondary: Colors.black, Color onSurface: Colors.white, Color onBackground: Colors.white, Color onError: Colors.black, Brightness brightness: Brightness.dark\})

Create the recommended dark color scheme that matches the [baseline Material color scheme][].

const

ColorScheme.fromSwatch(\{MaterialColor primarySwatch: Colors.blue, Color primaryColorDark, Color accentColor, Color cardColor, Color backgroundColor, Color errorColor, Brightness brightness: Brightness.light\})

Create a color scheme from a MaterialColor swatch. \[...\]

factory

ColorScheme.highContrastDark(\{Color primary: const Color(0xffefb7ff), Color primaryVariant: const Color(0xffbe9eff), Color secondary: const Color(0xff66fff9), Color secondaryVariant: const Color(0xff66fff9), Color surface: const Color(0xff121212), Color background: const Color(0xff121212), Color error: const Color(0xff9b374d), Color onPrimary: Colors.black, Color onSecondary: Colors.black, Color onSurface: Colors.white, Color onBackground: Colors.white, Color onError: Colors.black, Brightness brightness: Brightness.dark\})

Create a high contrast ColorScheme based on the dark [baseline Material color scheme][].

const

ColorScheme.highContrastLight(\{Color primary: const Color(0xff0000ba), Color primaryVariant: const Color(0xff000088), Color secondary: const Color(0xff66fff9), Color secondaryVariant: const Color(0xff018786), Color surface: Colors.white, Color background: Colors.white, Color error: const Color(0xff790000), Color onPrimary: Colors.white, Color onSecondary: Colors.black, Color onSurface: Colors.black, Color onBackground: Colors.black, Color onError: Colors.white, Brightness brightness: Brightness.light\})

Create a high contrast ColorScheme based on a purple primary color that matches the [baseline Material color scheme][baseline Material color scheme 1].

const

ColorScheme.light(\{Color primary: const Color(0xff6200ee), Color primaryVariant: const Color(0xff3700b3), Color secondary: const Color(0xff03dac6), Color secondaryVariant: const Color(0xff018786), Color surface: Colors.white, Color background: Colors.white, Color error: const Color(0xffb00020), Color onPrimary: Colors.white, Color onSecondary: Colors.black, Color onSurface: Colors.black, Color onBackground: Colors.black, Color onError: Colors.white, Brightness brightness: Brightness.light\})

Create a ColorScheme based on a purple primary color that matches the [baseline Material color scheme][baseline Material color scheme 1].

const

## Properties ##

background → Color

A color that typically appears behind scrollable content.

final

brightness → Brightness

The overall brightness of this color scheme.

final

error → Color

The color to use for input validation errors, e.g. for InputDecoration.errorText.

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

onBackground → Color

A color that's clearly legible when drawn on background. \[...\]

final

onError → Color

A color that's clearly legible when drawn on error. \[...\]

final

onPrimary → Color

A color that's clearly legible when drawn on primary. \[...\]

final

onSecondary → Color

A color that's clearly legible when drawn on secondary. \[...\]

final

onSurface → Color

A color that's clearly legible when drawn on surface. \[...\]

final

primary → Color

The color displayed most frequently across your app’s screens and components.

final

primaryVariant → Color

A darker version of the primary color.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

secondary → Color

An accent color that, when used sparingly, calls attention to parts of your app.

final

secondaryVariant → Color

A darker version of the secondary color.

final

surface → Color

The background color for widgets like Card.

final

## Methods ##

copyWith(\{Color primary, Color primaryVariant, Color secondary, Color secondaryVariant, Color surface, Color background, Color error, Color onPrimary, Color onSecondary, Color onSurface, Color onBackground, Color onError, Brightness brightness\}) → ColorScheme

Creates a copy of this color scheme with the given fields replaced by the non-null parameter values.

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

override

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

lerp(ColorScheme a, ColorScheme b, double t) → ColorScheme

Linearly interpolate between two ColorScheme objects. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/color_scheme.dart#L21
[Material spec]: https://material.io/design/color/the-color-system.html
[baseline Material color scheme]: https://material.io/design/color/dark-theme.html#ui-application
[baseline Material color scheme 1]: https://material.io/design/color/the-color-system.html#color-theme-creation