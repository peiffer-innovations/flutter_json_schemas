[*description*][description]

# BottomSheetThemeData class #

Defines default property values for BottomSheet's Material.

Descendant widgets obtain the current BottomSheetThemeData object using `Theme.of(context).bottomSheetTheme`. Instances of BottomSheetThemeData can be customized with BottomSheetThemeData.copyWith.

Typically a BottomSheetThemeData is specified as part of the overall Theme with ThemeData.bottomSheetTheme.

All BottomSheetThemeData properties are `null` by default. When null, the BottomSheet will provide its own defaults.

See also:

 *  ThemeData, which describes the overall theme information for the application.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

BottomSheetThemeData(\{Color backgroundColor, double elevation, Color modalBackgroundColor, double modalElevation, ShapeBorder shape, Clip clipBehavior\})

Creates a theme that can be used for ThemeData.bottomSheetTheme.

const

## Properties ##

backgroundColor → Color

Default value for BottomSheet.backgroundColor. \[...\]

final

clipBehavior → Clip

Default value for BottomSheet.clipBehavior. \[...\]

final

elevation → double

Default value for BottomSheet.elevation. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

modalBackgroundColor → Color

Value for BottomSheet.backgroundColor when the Bottom sheet is presented as a modal bottom sheet.

final

modalElevation → double

Value for BottomSheet.elevation when the Bottom sheet is presented as a modal bottom sheet.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

shape → ShapeBorder

Default value for BottomSheet.shape. \[...\]

final

## Methods ##

copyWith(\{Color backgroundColor, double elevation, Color modalBackgroundColor, double modalElevation, ShapeBorder shape, Clip clipBehavior\}) → BottomSheetThemeData

Creates a copy of this object with the given fields replaced with the new values.

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

lerp(BottomSheetThemeData a, BottomSheetThemeData b, double t) → BottomSheetThemeData

Linearly interpolate between two bottom sheet themes. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/bottom_sheet_theme.dart#L30