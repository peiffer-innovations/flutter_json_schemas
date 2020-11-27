[*description*][description]

# DialogTheme class #

Defines a theme for Dialog widgets.

Descendant widgets obtain the current DialogTheme object using `DialogTheme.of(context)`. Instances of DialogTheme can be customized with DialogTheme.copyWith.

When Shape is `null`, the dialog defaults to a RoundedRectangleBorder with a border radius of 2.0 on all corners.

titleTextStyle and contentTextStyle are used in AlertDialogs. If null, they default to TextTheme.headline6 and TextTheme.subtitle1, respectively.

See also:

 *  Dialog, a material dialog that can be customized using this DialogTheme.
 *  ThemeData, which describes the overall theme information for the application.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

DialogTheme(\{Color backgroundColor, double elevation, ShapeBorder shape, TextStyle titleTextStyle, TextStyle contentTextStyle\})

Creates a dialog theme that can be used for ThemeData.dialogTheme.

const

## Properties ##

backgroundColor → Color

Default value for Dialog.backgroundColor. \[...\]

final

contentTextStyle → TextStyle

Used to configure the DefaultTextStyle for the AlertDialog.content widget. \[...\]

final

elevation → double

Default value for Dialog.elevation. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

shape → ShapeBorder

Default value for Dialog.shape.

final

titleTextStyle → TextStyle

Used to configure the DefaultTextStyle for the AlertDialog.title widget. \[...\]

final

## Methods ##

copyWith(\{Color backgroundColor, double elevation, ShapeBorder shape, TextStyle titleTextStyle, TextStyle contentTextStyle\}) → DialogTheme

Creates a copy of this object but with the given fields replaced with the new values.

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

lerp(DialogTheme a, DialogTheme b, double t) → DialogTheme

Linearly interpolate between two dialog themes. \[...\]

of(BuildContext context) → DialogTheme

The data from the closest DialogTheme instance given the build context.


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/dialog_theme.dart#L33