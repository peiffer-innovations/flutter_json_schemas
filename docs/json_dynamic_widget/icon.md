[*description*][description]

# Icon class #

A graphical icon widget drawn with a glyph from a font described in an IconData such as material's predefined IconDatas in Icons.

Icons are not interactive. For an interactive icon, consider material's IconButton.

There must be an ambient Directionality widget when using Icon. Typically this is introduced automatically by the WidgetsApp or MaterialApp.

This widget assumes that the rendered icon is squared. Non-squared icons may render incorrectly.

 *link* 

Sample

This example shows how to create a Row of Icons in different colors and sizes. The first Icon uses a semanticLabel to announce in accessibility modes like TalkBack and VoiceOver.

![A row of icons representing a pink heart, a green musical note, and a blue umbrella][A row of icons representing a pink heart_ a green musical note_ and a blue umbrella]

*assignment*

    Row(
      mainAxisAlignment: MainAxisAlignment.spaceAround,
      children: const <Widget>[
        Icon(
          Icons.favorite,
          color: Colors.pink,
          size: 24.0,
          semanticLabel: 'Text to announce in accessibility modes',
        ),
        Icon(
          Icons.audiotrack,
          color: Colors.green,
          size: 30.0,
        ),
        Icon(
          Icons.beach_access,
          color: Colors.blue,
          size: 36.0,
        ),
      ],
    )

See also:

 *  IconButton, for interactive icons.
 *  Icons, for the list of available icons for use with this class.
 *  IconTheme, which provides ambient configuration for icons.
 *  ImageIcon, for showing icons from AssetImages or other ImageProviders.

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatelessWidget
 *  Icon

## Constructors ##

Icon(IconData icon, \{Key key, double size, Color color, String semanticLabel, TextDirection textDirection\})

Creates an icon. \[...\]

const

## Properties ##

color → Color

The color to use when drawing the icon. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

icon → IconData

The icon to display. The available icons are described in Icons. \[...\]

final

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

semanticLabel → String

Semantic label for the icon. \[...\]

final

size → double

The size of the icon in logical pixels. \[...\]

final

textDirection → TextDirection

The text direction to use for rendering the icon. \[...\]

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/icon.dart#L68
[A row of icons representing a pink heart_ a green musical note_ and a blue umbrella]: https://flutter.github.io/assets-for-api-docs/assets/widgets/icon.png