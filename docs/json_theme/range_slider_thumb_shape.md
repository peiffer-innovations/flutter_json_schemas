[*description*][description]

# RangeSliderThumbShape class #

Base class for RangeSlider thumb shapes.

See also:

 *  RoundRangeSliderThumbShape for the default RangeSlider's thumb shape that paints a solid circle.
 *  RangeSliderTickMarkShape, which can be used to create custom shapes for the RangeSlider's tick marks.
 *  RangeSliderTrackShape, which can be used to create custom shapes for the RangeSlider's track.
 *  RangeSliderValueIndicatorShape, which can be used to create custom shapes for the RangeSlider's value indicator.
 *  SliderComponentShape, which can be used to create custom shapes for the Slider's thumb, overlay, and value indicator and the RangeSlider's overlay.

Implementers

 *  RoundRangeSliderThumbShape

## Constructors ##

RangeSliderThumbShape()

This abstract const constructor enables subclasses to provide const constructors so that they can be used in const expressions.

const

## Properties ##

hashCode → int

The hash code for this object. \[...\]

read-only, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

getPreferredSize(bool isEnabled, bool isDiscrete) → Size

Returns the preferred size of the shape, based on the given conditions. \[...\]

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

paint(PaintingContext context, Offset center, \{Animation<double> activationAnimation, Animation<double> enableAnimation, bool isDiscrete, bool isEnabled, bool isOnTop, TextDirection textDirection, SliderThemeData sliderTheme, Thumb thumb, bool isPressed\}) → void

Paints the thumb shape based on the state passed to it. \[...\]

toString() → String

Returns a string representation of this object.

inherited

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/slider_theme.dart#L1075