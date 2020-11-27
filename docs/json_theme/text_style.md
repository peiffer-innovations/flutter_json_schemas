[*description*][description]

# TextStyle class Null safety #

An immutable style describing how to format and paint text.

### Bold ###

 *link* 

Sample

Here, a single line of text in a Text widget is given a specific style override. The style is mixed with the ambient DefaultTextStyle by the Text widget.

![Applying the style in this way creates bold text.][]

*assignment*

    Text(
      'No, we need bold strokes. We need this plan.',
      style: TextStyle(fontWeight: FontWeight.bold),
    )

### Italics ###

 *link* 

Sample

As in the previous example, the Text widget is given a specific style override which is implicitly mixed with the ambient DefaultTextStyle.

![This results in italicized text.][]

*assignment*

    Text(
      "Welcome to the present, we're running a real nation.",
      style: TextStyle(fontStyle: FontStyle.italic),
    )

### Opacity and Color ###

Each line here is progressively more opaque. The base color is material.Colors.black, and Color.withOpacity is used to create a derivative color with the desired opacity. The root TextSpan for this RichText widget is explicitly given the ambient DefaultTextStyle, since RichText does not do that automatically. The inner TextStyle objects are implicitly mixed with the parent TextSpan's TextSpan.style.

If color is specified, foreground must be null and vice versa. color is treated as a shorthand for `Paint()..color = color`.

If backgroundColor is specified, background must be null and vice versa. The backgroundColor is treated as a shorthand for `background: Paint()..color = backgroundColor`.

![This results in three lines of text that go from lighter to darker in color.][]

    RichText(
      text: TextSpan(
        style: DefaultTextStyle.of(context).style,
        children: <TextSpan>[
          TextSpan(
            text: "You don't have the votes.\n",
            style: TextStyle(color: Colors.black.withOpacity(0.6)),
          ),
          TextSpan(
            text: "You don't have the votes!\n",
            style: TextStyle(color: Colors.black.withOpacity(0.8)),
          ),
          TextSpan(
            text: "You're gonna need congressional approval and you don't have the votes!\n",
            style: TextStyle(color: Colors.black.withOpacity(1.0)),
          ),
        ],
      ),
    )

### Size ###

 *link* 

Sample

In this example, the ambient DefaultTextStyle is explicitly manipulated to obtain a TextStyle that doubles the default font size.

![This results in text that is twice as large as normal.][]

*assignment*

    Text(
      "These are wise words, enterprising men quote 'em.",
      style: DefaultTextStyle.of(context).style.apply(fontSizeFactor: 2.0),
    )

### Line height ###

By default, text will layout with line height as defined by the font. Font-metrics defined line height may be taller or shorter than the font size. The height property allows manual adjustment of the height of the line as a multiple of fontSize. For most fonts, setting height to 1.0 is not the same as omitting or setting height to null. The following diagram illustrates the difference between the font-metrics defined line height and the line height produced with `height: 1.0` (also known as the EM-square):

![Text height diagram][]

 *link* 

Sample

The height property can be used to change the line height. Here, the line height is set to 5 times the font size, so that the text is very spaced out. Since the `fontSize` is set to 10, the final height of the line is 50 pixels.

*assignment*

    Text(
      'Ladies and gentlemen, you coulda been anywhere in the world tonight, but you’re here with us in New York City.',
      style: TextStyle(height: 5, fontSize: 10),
    )

Examples of the resulting heights from different values of `TextStyle.height`:

![Text height comparison diagram][]

See StrutStyle for further control of line height at the paragraph level.

### Wavy red underline with black text ###

 *link* 

Sample

Styles can be combined. In this example, the misspelled word is drawn in black text and underlined with a wavy red line to indicate a spelling error. (The remainder is styled according to the Flutter default text styles, not the ambient DefaultTextStyle, since no explicit style is given and RichText does not automatically use the ambient DefaultTextStyle.)

![text_style_wavy_red_underline.png][]

*assignment*

    RichText(
      text: TextSpan(
        text: "Don't tax the South ",
        children: <TextSpan>[
          TextSpan(
            text: 'cuz',
            style: TextStyle(
              color: Colors.black,
              decoration: TextDecoration.underline,
              decorationColor: Colors.red,
              decorationStyle: TextDecorationStyle.wavy,
            ),
          ),
          TextSpan(
            text: ' we got it made in the shade',
          ),
        ],
      ),
    )

### Borders and stroke (Foreground) ###

 *link* 

Sample

To create bordered text, a Paint with Paint.style set to PaintingStyle.stroke should be provided as a foreground paint. The following example uses a Stack to produce a stroke and fill effect.

![Text border][]

*assignment*

    Stack(
      children: <Widget>[
        // Stroked text as border.
        Text(
          'Greetings, planet!',
          style: TextStyle(
            fontSize: 40,
            foreground: Paint()
              ..style = PaintingStyle.stroke
              ..strokeWidth = 6
              ..color = Colors.blue[700],
          ),
        ),
        // Solid text as fill.
        Text(
          'Greetings, planet!',
          style: TextStyle(
            fontSize: 40,
            color: Colors.grey[300],
          ),
        ),
      ],
    )

### Gradients (Foreground) ###

 *link* 

Sample

The foreground property also allows effects such as gradients to be applied to the text. Here we provide a Paint with a ui.Gradient shader.

![Text gradient][]

*assignment*

    Text(
      'Greetings, planet!',
      style: TextStyle(
        fontSize: 40,
        foreground: Paint()
          ..shader = ui.Gradient.linear(
            const Offset(0, 20),
            const Offset(150, 20),
            <Color>[
              Colors.red,
              Colors.yellow,
            ],
          )
      ),
    )

### Custom Fonts ###

Custom fonts can be declared in the `pubspec.yaml` file as shown below:

    flutter:
      fonts:
        - family: Raleway
          fonts:
            - asset: fonts/Raleway-Regular.ttf
            - asset: fonts/Raleway-Medium.ttf
              weight: 500
            - asset: assets/fonts/Raleway-SemiBold.ttf
              weight: 600
         - family: Schyler
           fonts:
             - asset: fonts/Schyler-Regular.ttf
             - asset: fonts/Schyler-Italic.ttf
               style: italic

The `family` property determines the name of the font, which you can use in the fontFamily argument. The `asset` property is a path to the font file, relative to the `pubspec.yaml` file. The `weight` property specifies the weight of the glyph outlines in the file as an integer multiple of 100 between 100 and 900. This corresponds to the FontWeight class and can be used in the fontWeight argument. The `style` property specifies whether the outlines in the file are `italic` or `normal`. These values correspond to the FontStyle class and can be used in the fontStyle argument.

To select a custom font, create TextStyle using the fontFamily argument as shown in the example below:

 *link* 

Sample

![text_style_custom_fonts.png][]

*assignment*

    const TextStyle(fontFamily: 'Raleway')

To use a font family defined in a package, the `package` argument must be provided. For instance, suppose the font declaration above is in the `pubspec.yaml` of a package named `my_package` which the app depends on. Then creating the TextStyle is done as follows:

    const TextStyle(fontFamily: 'Raleway', package: 'my_package')

If the package internally uses the font it defines, it should still specify the `package` argument when creating the text style as in the example above.

A package can also provide font files without declaring a font in its `pubspec.yaml`. These files should then be in the `lib/` folder of the package. The font files will not automatically be bundled in the app, instead the app can use these selectively when declaring a font. Suppose a package named `my_package` has:

    lib/fonts/Raleway-Medium.ttf

Then the app can declare a font like in the example below:

    flutter:
      fonts:
        - family: Raleway
          fonts:
            - asset: assets/fonts/Raleway-Regular.ttf
            - asset: packages/my_package/fonts/Raleway-Medium.ttf
              weight: 500

The `lib/` is implied, so it should not be included in the asset path.

In this case, since the app locally defines the font, the TextStyle is created without the `package` argument:

 *link* 

Sample

*assignment*

    const TextStyle(fontFamily: 'Raleway')

### Custom Font Fallback ###

A custom fontFamilyFallback list can be provided. The list should be an ordered list of strings of font family names in the order they will be attempted.

The fonts in fontFamilyFallback will be used only if the requested glyph is not present in the fontFamily.

The fallback order is:

 *  fontFamily
 *  fontFamilyFallback in order of first to last.
 *  System fallback fonts which will vary depending on platform.

The glyph used will always be the first matching version in fallback order.

The fontFamilyFallback property is commonly used to specify different font families for multilingual text spans as well as separate fonts for glyphs such as emojis.

 *link* 

Sample

In the following example, any glyphs not present in the font `Raleway` will be attempted to be resolved with `Noto Sans CJK SC`, and then with `Noto Color Emoji`:

*assignment*

    const TextStyle(
      fontFamily: 'Raleway',
      fontFamilyFallback: <String>[
        'Noto Sans CJK SC',
        'Noto Color Emoji',
      ],
    )

If all custom fallback font families are exhausted and no match was found or no custom fallback was provided, the platform font fallback will be used.

### Inconsistent platform fonts ###

Since Flutter's font discovery for default fonts depends on the fonts present on the device, it is not safe to assume all default fonts will be available or consistent across devices.

A known example of this is that Samsung devices ship with a CJK font that has smaller line spacing than the Android default. This results in Samsung devices displaying more tightly spaced text than on other Android devices when no custom font is specified.

To avoid this, a custom font should be specified if absolute font consistency is required for your application.

See also:

 *  Text, the widget for showing text in a single style.
 *  DefaultTextStyle, the widget that specifies the default text styles for Text widgets, configured using a TextStyle.
 *  RichText, the widget for showing a paragraph of mix-style text.
 *  TextSpan, the class that wraps a TextStyle for the purposes of passing it to a RichText.
 *  [TextStyle][], the class in the dart:ui library.
 *  Cookbook: [Use a custom font][]
 *  Cookbook: [Use themes to share colors and font styles][]

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

TextStyle(\{bool inherit: true, Color? color, Color? backgroundColor, double? fontSize, FontWeight? fontWeight, FontStyle? fontStyle, double? letterSpacing, double? wordSpacing, TextBaseline? textBaseline, double? height, Locale? locale, Paint? foreground, Paint? background, List<Shadow>? shadows, List<FontFeature>? fontFeatures, TextDecoration? decoration, Color? decorationColor, TextDecorationStyle? decorationStyle, double? decorationThickness, String? debugLabel, String? fontFamily, List<String>? fontFamilyFallback, String? package\})

Creates a text style. \[...\]

const

## Properties ##

background → Paint?

The paint drawn as a background for the text. \[...\]

final

backgroundColor → Color?

The color to use as the background for the text. \[...\]

final

color → Color?

The color to use when painting the text. \[...\]

final

debugLabel → String?

A human-readable description of this text style. \[...\]

final

decoration → TextDecoration?

The decorations to paint near the text (e.g., an underline). \[...\]

final

decorationColor → Color?

The color in which to paint the text decorations.

final

decorationStyle → TextDecorationStyle?

The style in which to paint the text decorations (e.g., dashed).

final

decorationThickness → double?

The thickness of the decoration stroke as a multiplier of the thickness defined by the font. \[...\]

final

fontFamily → String?

The name of the font to use when painting the text (e.g., Roboto). If the font is defined in a package, this will be prefixed with 'packages/package\_name/' (e.g. 'packages/cool\_fonts/Roboto'). The prefixing is done by the constructor when the `package` argument is provided. \[...\]

final

fontFamilyFallback → List<String>?

The ordered list of font families to fall back on when a glyph cannot be found in a higher priority font family. \[...\]

read-only

fontFeatures → List<FontFeature>?

A list of FontFeatures that affect how the font selects glyphs. \[...\]

final

fontSize → double?

The size of glyphs (in logical pixels) to use when painting the text. \[...\]

final

fontStyle → FontStyle?

The typeface variant to use when drawing the letters (e.g., italics).

final

fontWeight → FontWeight?

The typeface thickness to use when painting the text (e.g., bold).

final

foreground → Paint?

The paint drawn as a foreground for the text. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

height → double?

The height of this text span, as a multiple of the font size. \[...\]

final

inherit → bool

Whether null values are replaced with their value in an ancestor text style (e.g., in a TextSpan tree). \[...\]

final

letterSpacing → double?

The amount of space (in logical pixels) to add between each letter. A negative value can be used to bring the letters closer.

final

locale → Locale?

The locale used to select region-specific glyphs. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

shadows → List<Shadow>?

A list of Shadows that will be painted underneath the text. \[...\]

final

textBaseline → TextBaseline?

The common baseline that should be aligned between this text span and its parent text span, or, for the root text spans, with the line box.

final

wordSpacing → double?

The amount of space (in logical pixels) to add at each sequence of white-space (i.e. between each word). A negative value can be used to bring the words closer.

final

## Methods ##

apply(\{Color? color, Color? backgroundColor, TextDecoration? decoration, Color? decorationColor, TextDecorationStyle? decorationStyle, double decorationThicknessFactor: 1.0, double decorationThicknessDelta: 0.0, String? fontFamily, List<String>? fontFamilyFallback, double fontSizeFactor: 1.0, double fontSizeDelta: 0.0, int fontWeightDelta: 0, FontStyle? fontStyle, double letterSpacingFactor: 1.0, double letterSpacingDelta: 0.0, double wordSpacingFactor: 1.0, double wordSpacingDelta: 0.0, double heightFactor: 1.0, double heightDelta: 0.0, TextBaseline? textBaseline, Locale? locale, List<Shadow>? shadows, List<FontFeature>? fontFeatures\}) → TextStyle

Creates a copy of this text style replacing or altering the specified properties. \[...\]

compareTo(TextStyle other) → RenderComparison

Describe the difference between this style and another, in terms of how much damage it will make to the rendering. \[...\]

copyWith(\{bool? inherit, Color? color, Color? backgroundColor, String? fontFamily, List<String>? fontFamilyFallback, double? fontSize, FontWeight? fontWeight, FontStyle? fontStyle, double? letterSpacing, double? wordSpacing, TextBaseline? textBaseline, double? height, Locale? locale, Paint? foreground, Paint? background, List<Shadow>? shadows, List<FontFeature>? fontFeatures, TextDecoration? decoration, Color? decorationColor, TextDecorationStyle? decorationStyle, double? decorationThickness, String? debugLabel\}) → TextStyle

Creates a copy of this text style but with the given fields replaced with the new values. \[...\]

debugFillProperties(DiagnosticPropertiesBuilder properties, \{String prefix: ''\}) → void

Adds all properties prefixing property names with the optional `prefix`.

override

getParagraphStyle(\{TextAlign? textAlign, TextDirection? textDirection, double textScaleFactor: 1.0, String? ellipsis, int? maxLines, TextHeightBehavior? textHeightBehavior, Locale? locale, String? fontFamily, double? fontSize, FontWeight? fontWeight, FontStyle? fontStyle, double? height, StrutStyle? strutStyle\}) → ParagraphStyle

The style information for paragraphs, encoded for use by `dart:ui`. \[...\]

getTextStyle(\{double textScaleFactor: 1.0\}) → TextStyle

The style information for text runs, encoded for use by `dart:ui`.

merge(TextStyle? other) → TextStyle

Returns a new text style that is a combination of this style and the given `other` style. \[...\]

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

toDiagnosticsNode(\{String? name, DiagnosticsTreeStyle? style\}) → DiagnosticsNode

Returns a debug representation of the object that is used by debugging tools and by DiagnosticsNode.toStringDeep. \[...\]

inherited

toString(\{DiagnosticLevel minLevel: DiagnosticLevel.info\}) → String

Returns a string representation of this object.

inherited

toStringShort() → String

A brief description of this object, usually just the runtimeType and the hashCode. \[...\]

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

override

## Static Methods ##

lerp(TextStyle? a, TextStyle? b, double t) → TextStyle?

Interpolate between two text styles. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/painting/text_style.dart#L396
[Applying the style in this way creates bold text.]: https://flutter.github.io/assets-for-api-docs/assets/painting/text_style_bold.png
[This results in italicized text.]: https://flutter.github.io/assets-for-api-docs/assets/painting/text_style_italics.png
[This results in three lines of text that go from lighter to darker in color.]: https://flutter.github.io/assets-for-api-docs/assets/painting/text_style_opacity_and_color.png
[This results in text that is twice as large as normal.]: https://flutter.github.io/assets-for-api-docs/assets/painting/text_style_size.png
[Text height diagram]: https://flutter.github.io/assets-for-api-docs/assets/painting/text_height_diagram.png
[Text height comparison diagram]: https://flutter.github.io/assets-for-api-docs/assets/painting/text_height_comparison_diagram.png
[text_style_wavy_red_underline.png]: https://flutter.github.io/assets-for-api-docs/assets/painting/text_style_wavy_red_underline.png
[Text border]: https://flutter.github.io/assets-for-api-docs/assets/widgets/text_border.png
[Text gradient]: https://flutter.github.io/assets-for-api-docs/assets/widgets/text_gradient.png
[text_style_custom_fonts.png]: https://flutter.github.io/assets-for-api-docs/assets/painting/text_style_custom_fonts.png
[TextStyle]: https://api.flutter.dev/flutter/dart-ui/TextStyle-class.html
[Use a custom font]: https://flutter.dev/docs/cookbook/design/fonts
[Use themes to share colors and font styles]: https://flutter.dev/docs/cookbook/design/themes