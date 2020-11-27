[*description*][description]

# ShowValueIndicator enum #

Describes the conditions under which the value indicator on a Slider will be shown. Used with SliderThemeData.showValueIndicator.

See also:

 *  Slider, a Material Design slider widget.
 *  SliderThemeData, which describes the actual configuration of a slider theme.

## Constants ##

always → const ShowValueIndicator

The value indicator will be shown for all types of sliders.

`const ShowValueIndicator(2)`

never → const ShowValueIndicator

The value indicator will never be shown.

`const ShowValueIndicator(3)`

onlyForContinuous → const ShowValueIndicator

The value indicator will only be shown for continuous sliders (sliders where Slider.divisions is null).

`const ShowValueIndicator(1)`

onlyForDiscrete → const ShowValueIndicator

The value indicator will only be shown for discrete sliders (sliders where Slider.divisions is non-null).

`const ShowValueIndicator(0)`

values → const List<ShowValueIndicator>

A constant List of the values in this enum, in order of their declaration.

`const List<ShowValueIndicator>`

## Properties ##

hashCode → int

The hash code for this object. \[...\]

read-only, inherited

index → int

The integer index of this enum.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

toString() → String

Returns a string representation of this object.

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/slider_theme.dart#L138