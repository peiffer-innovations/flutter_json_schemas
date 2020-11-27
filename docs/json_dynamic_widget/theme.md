[*description*][description]

# Theme class #

Applies a theme to descendant widgets.

A theme describes the colors and typographic choices of an application.

Descendant widgets obtain the current theme's ThemeData object using Theme.of. When a widget uses Theme.of, it is automatically rebuilt if the theme later changes, so that the changes can be applied.

The Theme widget implies an IconTheme widget, set to the value of the ThemeData.iconTheme of the data for the Theme.

See also:

 *  ThemeData, which describes the actual configuration of a theme.
 *  AnimatedTheme, which animates the ThemeData when it changes rather than changing the theme all at once.
 *  MaterialApp, which includes an AnimatedTheme widget configured via the MaterialApp.theme argument.

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatelessWidget
 *  Theme

## Constructors ##

Theme(\{Key key, @required ThemeData data, bool isMaterialAppTheme: false, @required Widget child\})

Applies the given theme `data` to `child`. \[...\]

const

## Properties ##

child → Widget

The widget below this widget in the tree. \[...\]

final

data → ThemeData

Specifies the color and typography values for descendant widgets.

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

isMaterialAppTheme → bool

True if this theme was installed by the MaterialApp. \[...\]

final

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

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

## Static Methods ##

of(BuildContext context, \{bool shadowThemeOnly: false\}) → ThemeData

The data from the closest Theme instance that encloses the given context. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/theme.dart#L38