[*description*][description]

# RangeSliderTickMarkShape class #

Base class for RangeSlider tick mark shapes.

This is a simplified version of SliderComponentShape with a SliderThemeData passed when getting the preferred size.

See also:

 *  RoundRangeSliderTickMarkShape for the default RangeSlider's tick mark shape that paints a solid circle.
 *  RangeSliderThumbShape, which can be used to create custom shapes for the RangeSlider's thumb.
 *  RangeSliderTrackShape, which can be used to create custom shapes for the RangeSlider's track.
 *  RangeSliderValueIndicatorShape, which can be used to create custom shapes for the RangeSlider's value indicator.
 *  SliderComponentShape, which can be used to create custom shapes for the Slider's thumb, overlay, and value indicator and the RangeSlider's overlay.

Implementers

 *  RoundRangeSliderTickMarkShape

## Constructors ##

RangeSliderTickMarkShape()

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

getPreferredSize(\{SliderThemeData sliderTheme, bool isEnabled\}) → Size

Returns the preferred size of the shape. \[...\]

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

paint(PaintingContext context, Offset center, \{RenderBox parentBox, SliderThemeData sliderTheme, Animation<double> enableAnimation, Offset startThumbCenter, Offset endThumbCenter, bool isEnabled, TextDirection textDirection\}) → void

Paints the slider track. \[...\]

toString() → String

Returns a string representation of this object.

inherited

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/slider_theme.dart#L1270