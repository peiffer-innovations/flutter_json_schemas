[*description*][description]

# ListTile class #

A single fixed-height row that typically contains some text as well as a leading or trailing icon.

A list tile contains one to three lines of text optionally flanked by icons or other widgets, such as check boxes. The icons (or other widgets) for the tile are defined with the leading and trailing parameters. The first line of text is not optional and is specified with title. The value of subtitle, which *is* optional, will occupy the space allocated for an additional line of text, or two lines if isThreeLine is true. If dense is true then the overall height of this tile and the size of the DefaultTextStyles that wrap the title and subtitle widget are reduced.

It is the responsibility of the caller to ensure that title does not wrap, and to ensure that subtitle doesn't wrap (if isThreeLine is false) or wraps to two lines (if it is true).

The heights of the leading and trailing widgets are constrained according to the [Material spec][]. An exception is made for one-line ListTiles for accessibility. Please see the example below to see how to adhere to both Material spec and accessibility requirements.

Note that leading and trailing widgets can expand as far as they wish horizontally, so ensure that they are properly constrained.

List tiles are typically used in ListViews, or arranged in Columns in Drawers and Cards.

Requires one of its ancestors to be a Material widget.

 *link* 

Sample

This example uses a ListView to demonstrate different configurations of ListTiles in Cards.

![Different variations of ListTile][]

*assignment*

    ListView(
      children: const <Widget>[
        Card(child: ListTile(title: Text('One-line ListTile'))),
        Card(
          child: ListTile(
            leading: FlutterLogo(),
            title: Text('One-line with leading widget'),
          ),
        ),
        Card(
          child: ListTile(
            title: Text('One-line with trailing widget'),
            trailing: Icon(Icons.more_vert),
          ),
        ),
        Card(
          child: ListTile(
            leading: FlutterLogo(),
            title: Text('One-line with both widgets'),
            trailing: Icon(Icons.more_vert),
          ),
        ),
        Card(
          child: ListTile(
            title: Text('One-line dense ListTile'),
            dense: true,
          ),
        ),
        Card(
          child: ListTile(
            leading: FlutterLogo(size: 56.0),
            title: Text('Two-line ListTile'),
            subtitle: Text('Here is a second line'),
            trailing: Icon(Icons.more_vert),
          ),
        ),
        Card(
          child: ListTile(
            leading: FlutterLogo(size: 72.0),
            title: Text('Three-line ListTile'),
            subtitle: Text(
              'A sufficiently long subtitle warrants three lines.'
            ),
            trailing: Icon(Icons.more_vert),
            isThreeLine: true,
          ),
        ),
      ],
    )

 *link* 

Sample

Tiles can be much more elaborate. Here is a tile which can be tapped, but which is disabled when the `_act` variable is not 2. When the tile is tapped, the whole row has an ink splash effect (see InkWell).

*assignment*

    int _act = 1;
    // ...
    ListTile(
      leading: const Icon(Icons.flight_land),
      title: const Text("Trix's airplane"),
      subtitle: _act != 2 ? const Text('The airplane is only in Act II.') : null,
      enabled: _act == 2,
      onTap: () { /* react to the tile being tapped */ }
    )

To be accessible, tappable leading and trailing widgets have to be at least 48x48 in size. However, to adhere to the Material spec, trailing and leading widgets in one-line ListTiles should visually be at most 32 (dense: true) or 40 (dense: false) in height, which may conflict with the accessibility requirement.

For this reason, a one-line ListTile allows the height of leading and trailing widgets to be constrained by the height of the ListTile. This allows for the creation of tappable leading and trailing widgets that are large enough, but it is up to the developer to ensure that their widgets follow the Material spec.

 *link* 

Sample

Here is an example of a one-line, non-dense ListTile with a tappable leading widget that adheres to accessibility requirements and the Material spec. To adjust the use case below for a one-line, dense ListTile, adjust the vertical padding to 8.0.

*assignment*

    ListTile(
      leading: GestureDetector(
        behavior: HitTestBehavior.translucent,
        onTap: () {},
        child: Container(
          width: 48,
          height: 48,
          padding: EdgeInsets.symmetric(vertical: 4.0),
          alignment: Alignment.center,
          child: CircleAvatar(),
        ),
      ),
      title: Text('title'),
      dense: false,
    ),

## The ListTile layout isn't exactly what I want ##

If the way ListTile pads and positions its elements isn't quite what you're looking for, it's easy to create custom list items with a combination of other widgets, such as Rows and Columns.

 *link* 

Interactive App Sample code

Here is an example of a custom list item that resembles a Youtube related video list item created with Expanded and Container widgets.

![Custom list item a][]

To create a local project with this code sample, run:  
flutter create --sample=material.ListTile.4 mysample

Here is an example of a custom list item that resembles a Youtube related video list item created with Expanded and Container widgets.

![Custom list item a][]

*assignment*

    class CustomListItem extends StatelessWidget {
      const CustomListItem({
        this.thumbnail,
        this.title,
        this.user,
        this.viewCount,
      });
    
      final Widget thumbnail;
      final String title;
      final String user;
      final int viewCount;
    
      @override
      Widget build(BuildContext context) {
        return Padding(
          padding: const EdgeInsets.symmetric(vertical: 5.0),
          child: Row(
            crossAxisAlignment: CrossAxisAlignment.start,
            children: <Widget>[
              Expanded(
                flex: 2,
                child: thumbnail,
              ),
              Expanded(
                flex: 3,
                child: _VideoDescription(
                  title: title,
                  user: user,
                  viewCount: viewCount,
                ),
              ),
              const Icon(
                Icons.more_vert,
                size: 16.0,
              ),
            ],
          ),
        );
      }
    }
    
    class _VideoDescription extends StatelessWidget {
      const _VideoDescription({
        Key key,
        this.title,
        this.user,
        this.viewCount,
      }) : super(key: key);
    
      final String title;
      final String user;
      final int viewCount;
    
      @override
      Widget build(BuildContext context) {
        return Padding(
          padding: const EdgeInsets.fromLTRB(5.0, 0.0, 0.0, 0.0),
          child: Column(
            crossAxisAlignment: CrossAxisAlignment.start,
            children: <Widget>[
              Text(
                title,
                style: const TextStyle(
                  fontWeight: FontWeight.w500,
                  fontSize: 14.0,
                ),
              ),
              const Padding(padding: EdgeInsets.symmetric(vertical: 2.0)),
              Text(
                user,
                style: const TextStyle(fontSize: 10.0),
              ),
              const Padding(padding: EdgeInsets.symmetric(vertical: 1.0)),
              Text(
                '$viewCount views',
                style: const TextStyle(fontSize: 10.0),
              ),
            ],
          ),
        );
      }
    }
    
    // ...
    
    Widget build(BuildContext context) {
      return ListView(
        padding: const EdgeInsets.all(8.0),
        itemExtent: 106.0,
        children: <CustomListItem>[
          CustomListItem(
            user: 'Flutter',
            viewCount: 999000,
            thumbnail: Container(
              decoration: const BoxDecoration(color: Colors.blue),
            ),
            title: 'The Flutter YouTube Channel',
          ),
          CustomListItem(
            user: 'Dash',
            viewCount: 884000,
            thumbnail: Container(
              decoration: const BoxDecoration(color: Colors.yellow),
            ),
            title: 'Announcing Flutter 1.0',
          ),
        ],
      );
    }

 *link* 

Interactive App Sample code

Here is an example of an article list item with multiline titles and subtitles. It utilizes Rows and Columns, as well as Expanded and AspectRatio widgets to organize its layout.

![Custom list item b][]

To create a local project with this code sample, run:  
flutter create --sample=material.ListTile.5 mysample

Here is an example of an article list item with multiline titles and subtitles. It utilizes Rows and Columns, as well as Expanded and AspectRatio widgets to organize its layout.

![Custom list item b][]

*assignment*

    class _ArticleDescription extends StatelessWidget {
      _ArticleDescription({
        Key key,
        this.title,
        this.subtitle,
        this.author,
        this.publishDate,
        this.readDuration,
      }) : super(key: key);
    
      final String title;
      final String subtitle;
      final String author;
      final String publishDate;
      final String readDuration;
    
      @override
      Widget build(BuildContext context) {
        return Column(
          crossAxisAlignment: CrossAxisAlignment.start,
          children: <Widget>[
            Expanded(
              flex: 1,
              child: Column(
                crossAxisAlignment: CrossAxisAlignment.start,
                children: <Widget>[
                  Text(
                    '$title',
                    maxLines: 2,
                    overflow: TextOverflow.ellipsis,
                    style: const TextStyle(
                      fontWeight: FontWeight.bold,
                    ),
                  ),
                  const Padding(padding: EdgeInsets.only(bottom: 2.0)),
                  Text(
                    '$subtitle',
                    maxLines: 2,
                    overflow: TextOverflow.ellipsis,
                    style: const TextStyle(
                      fontSize: 12.0,
                      color: Colors.black54,
                    ),
                  ),
                ],
              ),
            ),
            Expanded(
              flex: 1,
              child: Column(
                crossAxisAlignment: CrossAxisAlignment.start,
                mainAxisAlignment: MainAxisAlignment.end,
                children: <Widget>[
                  Text(
                    '$author',
                    style: const TextStyle(
                      fontSize: 12.0,
                      color: Colors.black87,
                    ),
                  ),
                  Text(
                    '$publishDate - $readDuration',
                    style: const TextStyle(
                      fontSize: 12.0,
                      color: Colors.black54,
                    ),
                  ),
                ],
              ),
            ),
          ],
        );
      }
    }
    
    class CustomListItemTwo extends StatelessWidget {
      CustomListItemTwo({
        Key key,
        this.thumbnail,
        this.title,
        this.subtitle,
        this.author,
        this.publishDate,
        this.readDuration,
      }) : super(key: key);
    
      final Widget thumbnail;
      final String title;
      final String subtitle;
      final String author;
      final String publishDate;
      final String readDuration;
    
      @override
      Widget build(BuildContext context) {
        return Padding(
          padding: const EdgeInsets.symmetric(vertical: 10.0),
          child: SizedBox(
            height: 100,
            child: Row(
              crossAxisAlignment: CrossAxisAlignment.start,
              children: <Widget>[
                AspectRatio(
                  aspectRatio: 1.0,
                  child: thumbnail,
                ),
                Expanded(
                  child: Padding(
                    padding: const EdgeInsets.fromLTRB(20.0, 0.0, 2.0, 0.0),
                    child: _ArticleDescription(
                      title: title,
                      subtitle: subtitle,
                      author: author,
                      publishDate: publishDate,
                      readDuration: readDuration,
                    ),
                  ),
                )
              ],
            ),
          ),
        );
      }
    }
    
    // ...
    
    Widget build(BuildContext context) {
      return ListView(
        padding: const EdgeInsets.all(10.0),
        children: <Widget>[
          CustomListItemTwo(
            thumbnail: Container(
              decoration: const BoxDecoration(color: Colors.pink),
            ),
            title: 'Flutter 1.0 Launch',
            subtitle:
              'Flutter continues to improve and expand its horizons.'
              'This text should max out at two lines and clip',
            author: 'Dash',
            publishDate: 'Dec 28',
            readDuration: '5 mins',
          ),
          CustomListItemTwo(
            thumbnail: Container(
              decoration: const BoxDecoration(color: Colors.blue),
            ),
            title: 'Flutter 1.2 Release - Continual updates to the framework',
            subtitle: 'Flutter once again improves and makes updates.',
            author: 'Flutter',
            publishDate: 'Feb 26',
            readDuration: '12 mins',
          ),
        ],
      );
    }

See also:

 *  ListTileTheme, which defines visual properties for ListTiles.
 *  ListView, which can display an arbitrary number of ListTiles in a scrolling list.
 *  CircleAvatar, which shows an icon representing a person and is often used as the leading element of a ListTile.
 *  Card, which can be used with Column to show a few ListTiles.
 *  Divider, which can be used to separate ListTiles.
 *  ListTile.divideTiles, a utility for inserting Dividers in between ListTiles.
 *  CheckboxListTile, RadioListTile, and SwitchListTile, widgets that combine ListTile with other controls.
 *  [material.io/design/components/lists.html][Material spec]
 *  Cookbook: [Use lists][]
 *  Cookbook: [Implement swipe to dismiss][]

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatelessWidget
 *  ListTile

## Constructors ##

ListTile(\{Key key, Widget leading, Widget title, Widget subtitle, Widget trailing, bool isThreeLine: false, bool dense, VisualDensity visualDensity, ShapeBorder shape, EdgeInsetsGeometry contentPadding, bool enabled: true, GestureTapCallback onTap, GestureLongPressCallback onLongPress, MouseCursor mouseCursor, bool selected: false, Color focusColor, Color hoverColor, FocusNode focusNode, bool autofocus: false, Color tileColor, Color selectedTileColor\})

Creates a list tile. \[...\]

const

## Properties ##

autofocus → bool

True if this widget will be selected as the initial focus when no other node in its scope is currently focused. \[...\]

final

contentPadding → EdgeInsetsGeometry

The tile's internal padding. \[...\]

final

dense → bool

Whether this list tile is part of a vertically dense list. \[...\]

final

enabled → bool

Whether this list tile is interactive. \[...\]

final

focusColor → Color

The color for the tile's Material when it has the input focus.

final

focusNode → FocusNode

An optional focus node to use as the focus node for this widget. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

hoverColor → Color

The color for the tile's Material when a pointer is hovering over it.

final

isThreeLine → bool

Whether this list tile is intended to display three lines of text. \[...\]

final

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

leading → Widget

A widget to display before the title. \[...\]

final

mouseCursor → MouseCursor

The cursor for a mouse pointer when it enters or is hovering over the widget. \[...\]

final

onLongPress → GestureLongPressCallback

Called when the user long-presses on this list tile. \[...\]

final

onTap → GestureTapCallback

Called when the user taps this list tile. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

selected → bool

If this tile is also enabled then icons and text are rendered with the same color. \[...\]

final

selectedTileColor → Color

Defines the background color of `ListTile` when selected is true. \[...\]

final

shape → ShapeBorder

The shape of the tile's InkWell. \[...\]

final

subtitle → Widget

Additional content displayed below the title. \[...\]

final

tileColor → Color

Defines the background color of `ListTile` when selected is false. \[...\]

final

title → Widget

The primary content of the list tile. \[...\]

final

trailing → Widget

A widget to display after the title. \[...\]

final

visualDensity → VisualDensity

Defines how compact the list tile's layout will be. \[...\]

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

## Static Methods ##

divideTiles(\{BuildContext context, Iterable<Widget> tiles, Color color\}) → Iterable<Widget>

Add a one pixel border in between each tile. If color isn't specified the ThemeData.dividerColor of the context's Theme is used. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/list_tile.dart#L659
[Material spec]: https://material.io/design/components/lists.html
[Different variations of ListTile]: https://flutter.github.io/assets-for-api-docs/assets/material/list_tile.png
[Custom list item a]: https://flutter.github.io/assets-for-api-docs/assets/widgets/custom_list_item_a.png
[Custom list item b]: https://flutter.github.io/assets-for-api-docs/assets/widgets/custom_list_item_b.png
[Use lists]: https://flutter.dev/docs/cookbook/lists/basic-list
[Implement swipe to dismiss]: https://flutter.dev/docs/cookbook/gestures/dismissible