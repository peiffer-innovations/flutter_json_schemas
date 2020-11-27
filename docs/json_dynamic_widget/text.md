[*description*][description]

# Text class #

A run of text with a single style.

The Text widget displays a string of text with single style. The string might break across multiple lines or might all be displayed on the same line depending on the layout constraints.

The style argument is optional. When omitted, the text will use the style from the closest enclosing DefaultTextStyle. If the given style's TextStyle.inherit property is true (the default), the given style will be merged with the closest enclosing DefaultTextStyle. This merging behavior is useful, for example, to make the text bold while using the default font family and size.

 *link* 

Sample

This example shows how to display text using the Text widget with the overflow set to TextOverflow.ellipsis.

![If the text is shorter than the available space, it is displayed in full without an ellipsis.][If the text is shorter than the available space_ it is displayed in full without an ellipsis.]

![If the text overflows, the Text widget displays an ellipsis to trim the overflowing text][If the text overflows_ the Text widget displays an ellipsis to trim the overflowing text]

*assignment*

    Text(
      'Hello, $_name! How are you?',
      textAlign: TextAlign.center,
      overflow: TextOverflow.ellipsis,
      style: TextStyle(fontWeight: FontWeight.bold),
    )

Using the Text.rich constructor, the Text widget can display a paragraph with differently styled TextSpans. The sample that follows displays "Hello beautiful world" with different styles for each word.

 *link* 

Sample

![The word][]

*assignment*

    const Text.rich(
      TextSpan(
        text: 'Hello', // default text style
        children: <TextSpan>[
          TextSpan(text: ' beautiful ', style: TextStyle(fontStyle: FontStyle.italic)),
          TextSpan(text: 'world', style: TextStyle(fontWeight: FontWeight.bold)),
        ],
      ),
    )

## Interactivity ##

To make Text react to touch events, wrap it in a GestureDetector widget with a GestureDetector.onTap handler.

In a material design application, consider using a TextButton instead, or if that isn't appropriate, at least using an InkWell instead of GestureDetector.

To make sections of the text interactive, use RichText and specify a TapGestureRecognizer as the TextSpan.recognizer of the relevant part of the text.

See also:

 *  RichText, which gives you more control over the text styles.
 *  DefaultTextStyle, which sets default styles for Text widgets.

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatelessWidget
 *  Text

## Constructors ##

Text(String data, \{Key key, TextStyle style, StrutStyle strutStyle, TextAlign textAlign, TextDirection textDirection, Locale locale, bool softWrap, TextOverflow overflow, double textScaleFactor, int maxLines, String semanticsLabel, TextWidthBasis textWidthBasis, TextHeightBehavior textHeightBehavior\})

Creates a text widget. \[...\]

const

Text.rich(InlineSpan textSpan, \{Key key, TextStyle style, StrutStyle strutStyle, TextAlign textAlign, TextDirection textDirection, Locale locale, bool softWrap, TextOverflow overflow, double textScaleFactor, int maxLines, String semanticsLabel, TextWidthBasis textWidthBasis, TextHeightBehavior textHeightBehavior\})

Creates a text widget with a InlineSpan. \[...\]

const

## Properties ##

data → String

The text to display. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

locale → Locale

Used to select a font when the same Unicode character can be rendered differently, depending on the locale. \[...\]

final

maxLines → int

An optional maximum number of lines for the text to span, wrapping if necessary. If the text exceeds the given number of lines, it will be truncated according to overflow. \[...\]

final

overflow → TextOverflow

How visual overflow should be handled. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

semanticsLabel → String

An alternative semantics label for this text. \[...\]

final

softWrap → bool

Whether the text should break at soft line breaks. \[...\]

final

strutStyle → StrutStyle

The strut style to use. Strut style defines the strut, which sets minimum vertical layout metrics. \[...\]

final

style → TextStyle

If non-null, the style to use for this text. \[...\]

final

textAlign → TextAlign

How the text should be aligned horizontally.

final

textDirection → TextDirection

The directionality of the text. \[...\]

final

textHeightBehavior → TextHeightBehavior

Defines how the paragraph will apply TextStyle.height to the ascent of the first line and descent of the last line. \[...\]

final

textScaleFactor → double

The number of font pixels for each logical pixel. \[...\]

final

textSpan → InlineSpan

The text to display as a InlineSpan. \[...\]

final

textWidthBasis → TextWidthBasis

Defines how to measure the width of the rendered text.

final

## Methods ##

build(BuildContext context) → Widget

Describes the part of the user interface represented by this widget. \[...\]

override

createElement() → StatelessElement

Creates a StatelessElement to manage this widget's location in the tree. \[...\]

inherited

debugDescribeChildren() → List<DiagnosticsNode>

Returns a list of DiagnosticsNode objects describing this node's children. \[...\]

@protected, inherited

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

toStringDeep(\{String prefixLineOne: '', String prefixOtherLines, DiagnosticLevel minLevel: DiagnosticLevel.debug\}) → String

Returns a string representation of this node and its descendants. \[...\]

inherited

toStringShallow(\{String joiner: ', ', DiagnosticLevel minLevel: DiagnosticLevel.debug\}) → String

Returns a one-line detailed description of the object. \[...\]

inherited

toStringShort() → String

A short, textual description of this widget.

inherited

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

@nonVirtual, inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/text.dart#L343
[If the text is shorter than the available space_ it is displayed in full without an ellipsis.]: https://flutter.github.io/assets-for-api-docs/assets/widgets/text.png
[If the text overflows_ the Text widget displays an ellipsis to trim the overflowing text]: https://flutter.github.io/assets-for-api-docs/assets/widgets/text_ellipsis.png
[The word]: https://flutter.github.io/assets-for-api-docs/assets/widgets/text_rich.png