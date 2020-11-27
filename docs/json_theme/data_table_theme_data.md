[*description*][description]

# DataTableThemeData class #

Defines default property values for descendant DataTable widgets.

Descendant widgets obtain the current DataTableThemeData object using `DataTableTheme.of(context)`. Instances of DataTableThemeData can be customized with DataTableThemeData.copyWith.

Typically a DataTableThemeData is specified as part of the overall Theme with ThemeData.dataTableTheme.

All DataTableThemeData properties are `null` by default. When null, the DataTable will use the values from ThemeData if they exist, otherwise it will provide its own defaults based on the overall Theme's textTheme and colorScheme. See the individual DataTable properties for details.

See also:

 *  ThemeData, which describes the overall theme information for the application.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

DataTableThemeData(\{MaterialStateProperty<Color> dataRowColor, double dataRowHeight, TextStyle dataTextStyle, MaterialStateProperty<Color> headingRowColor, double headingRowHeight, TextStyle headingTextStyle, double horizontalMargin, double columnSpacing, double dividerThickness\})

Creates a theme that can be used for ThemeData.dataTableTheme.

const

## Properties ##

columnSpacing → double

The horizontal margin between the contents of each data column.

final

dataRowColor → MaterialStateProperty<Color>

The background color for the data rows. \[...\]

final

dataRowHeight → double

The height of each row (excluding the row that contains column headings).

final

dataTextStyle → TextStyle

The text style for data rows.

final

dividerThickness → double

The width of the divider that appears between TableRows. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

headingRowColor → MaterialStateProperty<Color>

The background color for the heading row. \[...\]

final

headingRowHeight → double

The height of the heading row.

final

headingTextStyle → TextStyle

The text style for the heading row.

final

horizontalMargin → double

The horizontal margin between the edges of the table and the content in the first and last cells of each row. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

copyWith(\{MaterialStateProperty<Color> dataRowColor, double dataRowHeight, TextStyle dataTextStyle, MaterialStateProperty<Color> headingRowColor, double headingRowHeight, TextStyle headingTextStyle, double horizontalMargin, double columnSpacing, double dividerThickness\}) → DataTableThemeData

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

lerp(DataTableThemeData a, DataTableThemeData b, double t) → DataTableThemeData

Linearly interpolate between two DataTableThemeDatas. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/data_table_theme.dart#L37