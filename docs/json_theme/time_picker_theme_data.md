[*description*][description]

# TimePickerThemeData class #

Defines the visual properties of the widget displayed with showTimePicker.

Descendant widgets obtain the current TimePickerThemeData object using `TimePickerTheme.of(context)`. Instances of TimePickerThemeData can be customized with TimePickerThemeData.copyWith.

Typically a TimePickerThemeData is specified as part of the overall Theme with ThemeData.timePickerTheme.

All TimePickerThemeData properties are `null` by default. When null, showTimePicker will provide its own defaults.

See also:

 *  ThemeData, which describes the overall theme information for the application.
 *  TimePickerTheme, which describes the actual configuration of a time picker theme.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

TimePickerThemeData(\{Color backgroundColor, Color hourMinuteTextColor, Color hourMinuteColor, Color dayPeriodTextColor, Color dayPeriodColor, Color dialHandColor, Color dialBackgroundColor, Color dialTextColor, Color entryModeIconColor, TextStyle hourMinuteTextStyle, TextStyle dayPeriodTextStyle, TextStyle helpTextStyle, ShapeBorder shape, ShapeBorder hourMinuteShape, OutlinedBorder dayPeriodShape, BorderSide dayPeriodBorderSide, InputDecorationTheme inputDecorationTheme\})

Creates a theme that can be used for TimePickerTheme or ThemeData.timePickerTheme.

const

## Properties ##

backgroundColor → Color

The background color of a time picker. \[...\]

final

dayPeriodBorderSide → BorderSide

The color and weight of the day period's outline. \[...\]

final

dayPeriodColor → Color

The background color of the AM/PM toggle. \[...\]

final

dayPeriodShape → OutlinedBorder

The shape of the day period that the time picker uses. \[...\]

final

dayPeriodTextColor → Color

The color of the day period text that represents AM/PM. \[...\]

final

dayPeriodTextStyle → TextStyle

Used to configure the TextStyles for the day period control. \[...\]

final

dialBackgroundColor → Color

The background color of the time picker dial. \[...\]

final

dialHandColor → Color

The color of the time picker dial's hand. \[...\]

final

dialTextColor → Color

The color of the dial text that represents specific hours and minutes. \[...\]

final

entryModeIconColor → Color

The color of the entry mode IconButton. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

helpTextStyle → TextStyle

Used to configure the TextStyles for the helper text in the header. \[...\]

final

hourMinuteColor → Color

The background color of the hour and minutes header segments. \[...\]

final

hourMinuteShape → ShapeBorder

The shape of the hour and minute controls that the time picker uses. \[...\]

final

hourMinuteTextColor → Color

The color of the header text that represents hours and minutes. \[...\]

final

hourMinuteTextStyle → TextStyle

Used to configure the TextStyles for the hour/minute controls. \[...\]

final

inputDecorationTheme → InputDecorationTheme

The input decoration theme for the TextFields in the time picker. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

shape → ShapeBorder

The shape of the Dialog that the time picker is presented in. \[...\]

final

## Methods ##

copyWith(\{Color backgroundColor, Color hourMinuteTextColor, Color hourMinuteColor, Color dayPeriodTextColor, Color dayPeriodColor, Color dialHandColor, Color dialBackgroundColor, Color dialTextColor, Color entryModeIconColor, TextStyle hourMinuteTextStyle, TextStyle dayPeriodTextStyle, TextStyle helpTextStyle, ShapeBorder shape, ShapeBorder hourMinuteShape, OutlinedBorder dayPeriodShape, BorderSide dayPeriodBorderSide, InputDecorationTheme inputDecorationTheme\}) → TimePickerThemeData

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

lerp(TimePickerThemeData a, TimePickerThemeData b, double t) → TimePickerThemeData

Linearly interpolate between two time picker themes. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/time_picker_theme.dart#L32