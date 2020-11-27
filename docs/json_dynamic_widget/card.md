[*description*][description]

# Card class #

A material design card: a panel with slightly rounded corners and an elevation shadow.

A card is a sheet of Material used to represent some related information, for example an album, a geographical location, a meal, contact details, etc.

This is what it looks like when run:

![A card with a slight shadow, consisting of two rows, one with an icon and some text describing a musical, and the other with buttons for buying tickets or listening to the show.][A card with a slight shadow_ consisting of two rows_ one with an icon and some text describing a musical_ and the other with buttons for buying tickets or listening to the show.]

 *link* 

Interactive App Sample code

This sample shows creation of a Card widget that shows album information and two actions.

To create a local project with this code sample, run:  
flutter create --sample=material.Card.1 mysample

This sample shows creation of a Card widget that shows album information and two actions.

*assignment*

    Widget build(BuildContext context) {
      return Center(
        child: Card(
          child: Column(
            mainAxisSize: MainAxisSize.min,
            children: <Widget>[
              const ListTile(
                leading: Icon(Icons.album),
                title: Text('The Enchanted Nightingale'),
                subtitle: Text('Music by Julie Gable. Lyrics by Sidney Stein.'),
              ),
              Row(
                mainAxisAlignment: MainAxisAlignment.end,
                children: <Widget>[
                  TextButton(
                    child: const Text('BUY TICKETS'),
                    onPressed: () { /* ... */ },
                  ),
                  const SizedBox(width: 8),
                  TextButton(
                    child: const Text('LISTEN'),
                    onPressed: () { /* ... */ },
                  ),
                  const SizedBox(width: 8),
                ],
              ),
            ],
          ),
        ),
      );
    }

Sometimes the primary action area of a card is the card itself. Cards can be one large touch target that shows a detail screen when tapped.

 *link* 

Interactive App Sample code

This sample shows creation of a Card widget that can be tapped. When tapped this Card's InkWell displays an "ink splash" that fills the entire card.

To create a local project with this code sample, run:  
flutter create --sample=material.Card.2 mysample

This sample shows creation of a Card widget that can be tapped. When tapped this Card's InkWell displays an "ink splash" that fills the entire card.

*assignment*

    Widget build(BuildContext context) {
      return Center(
        child: Card(
          child: InkWell(
            splashColor: Colors.blue.withAlpha(30),
            onTap: () {
              print('Card tapped.');
            },
            child: Container(
              width: 300,
              height: 100,
              child: Text('A card that can be tapped'),
            ),
          ),
        ),
      );
    }

See also:

 *  ListTile, to display icons and text in a card.
 *  showDialog, to display a modal card.
 *  [material.io/design/components/cards.html][material.io_design_components_cards.html]

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatelessWidget
 *  Card

## Constructors ##

Card(\{Key key, Color color, Color shadowColor, double elevation, ShapeBorder shape, bool borderOnForeground: true, EdgeInsetsGeometry margin, Clip clipBehavior, Widget child, bool semanticContainer: true\})

Creates a material design card. \[...\]

const

## Properties ##

borderOnForeground → bool

Whether to paint the shape border in front of the child. \[...\]

final

child → Widget

The widget below this widget in the tree. \[...\]

final

clipBehavior → Clip

The content will be clipped (or not) according to this option. \[...\]

final

color → Color

The card's background color. \[...\]

final

elevation → double

The z-coordinate at which to place this card. This controls the size of the shadow below the card. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

margin → EdgeInsetsGeometry

The empty space that surrounds the card. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

semanticContainer → bool

Whether this widget represents a single semantic container, or if false a collection of individual semantic nodes. \[...\]

final

shadowColor → Color

The color to paint the shadow below the card. \[...\]

final

shape → ShapeBorder

The shape of the card's Material. \[...\]

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

inherited

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/card.dart#L101
[A card with a slight shadow_ consisting of two rows_ one with an icon and some text describing a musical_ and the other with buttons for buying tickets or listening to the show.]: https://flutter.github.io/assets-for-api-docs/assets/material/card.png
[material.io_design_components_cards.html]: https://material.io/design/components/cards.html