[*description*][description]

# CupertinoTextThemeData class #

Cupertino typography theme in a CupertinoThemeData.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

CupertinoTextThemeData(\{Color primaryColor: CupertinoColors.systemBlue, @Deprecated('This argument no longer does anything. You can remove it. ' 'This feature was deprecated after v1.10.14.') Brightness brightness, TextStyle textStyle, TextStyle actionTextStyle, TextStyle tabLabelTextStyle, TextStyle navTitleTextStyle, TextStyle navLargeTitleTextStyle, TextStyle navActionTextStyle, TextStyle pickerTextStyle, TextStyle dateTimePickerTextStyle\})

Create a CupertinoTextThemeData. \[...\]

const

## Properties ##

actionTextStyle → TextStyle

The TextStyle of interactive text content such as text in a button without background.

read-only

dateTimePickerTextStyle → TextStyle

The TextStyle of date time pickers.

read-only

hashCode → int

The hash code for this object. \[...\]

read-only, inherited

navActionTextStyle → TextStyle

The TextStyle of interactive text content in navigation bars.

read-only

navLargeTitleTextStyle → TextStyle

The TextStyle of large titles in sliver navigation bars.

read-only

navTitleTextStyle → TextStyle

The TextStyle of titles in standard navigation bars.

read-only

pickerTextStyle → TextStyle

The TextStyle of pickers.

read-only

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

tabLabelTextStyle → TextStyle

The TextStyle of unselected tabs.

read-only

textStyle → TextStyle

The TextStyle of general text content for Cupertino widgets.

read-only

## Methods ##

copyWith(\{Color primaryColor, Brightness brightness, TextStyle textStyle, TextStyle actionTextStyle, TextStyle tabLabelTextStyle, TextStyle navTitleTextStyle, TextStyle navLargeTitleTextStyle, TextStyle navActionTextStyle, TextStyle pickerTextStyle, TextStyle dateTimePickerTextStyle\}) → CupertinoTextThemeData

Returns a copy of the current CupertinoTextThemeData instance with specified overrides.

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

override

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

resolveFrom(BuildContext context, \{bool nullOk: false\}) → CupertinoTextThemeData

Returns a copy of the current CupertinoTextThemeData with all the colors resolved against the given BuildContext. \[...\]

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

inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/cupertino/text_theme.dart#L112