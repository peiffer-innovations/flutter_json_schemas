[*description*][description]

# TextSelectionThemeData class #

Defines the visual properties needed for text selection in TextField and SelectableText widgets.

Used by TextSelectionTheme to control the visual properties of text selection in a widget subtree.

Use TextSelectionTheme.of to access the closest ancestor TextSelectionTheme of the current BuildContext.

See also:

 *  TextSelectionTheme, an InheritedWidget that propagates the theme down its subtree.
 *  InputDecorationTheme, which defines most other visual properties of text fields.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

TextSelectionThemeData(\{Color cursorColor, Color selectionColor, Color selectionHandleColor\})

Creates the set of properties used to configure TextFields.

const

## Properties ##

cursorColor → Color

The color of the cursor in the text field. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

selectionColor → Color

The background color of selected text.

final

selectionHandleColor → Color

The color of the selection handles on the text field. \[...\]

final

## Methods ##

copyWith(\{Color cursorColor, Color selectionColor, Color selectionHandleColor\}) → TextSelectionThemeData

Creates a copy of this object with the given fields replaced with the specified values.

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

lerp(TextSelectionThemeData a, TextSelectionThemeData b, double t) → TextSelectionThemeData

Linearly interpolate between two text field themes. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/text_selection_theme.dart#L28