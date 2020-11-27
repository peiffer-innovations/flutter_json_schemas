[*description*][description]

# RangeSliderValueIndicatorShape class #

Base class for RangeSlider value indicator shapes.

See also:

 *  PaddleRangeSliderValueIndicatorShape for the default RangeSlider's value indicator shape that paints a custom path with text in it.
 *  RangeSliderTickMarkShape, which can be used to create custom shapes for the RangeSlider's tick marks.
 *  RangeSliderThumbShape, which can be used to create custom shapes for the RangeSlider's thumb.
 *  RangeSliderTrackShape, which can be used to create custom shapes for the RangeSlider's track.
 *  SliderComponentShape, which can be used to create custom shapes for the Slider's thumb, overlay, and value indicator and the RangeSlider's overlay.

Implementers

 *  PaddleRangeSliderValueIndicatorShape
 *  RectangularRangeSliderValueIndicatorShape

## Constructors ##

RangeSliderValueIndicatorShape()

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

getHorizontalShift(\{RenderBox parentBox, Offset center, TextPainter labelPainter, Animation<double> activationAnimation, double textScaleFactor, Size sizeWithOverflow\}) → double

Determines the best offset to keep this shape on the screen. \[...\]

getPreferredSize(bool isEnabled, bool isDiscrete, \{TextPainter labelPainter, double textScaleFactor\}) → Size

Returns the preferred size of the shape, based on the given conditions. \[...\]

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

paint(PaintingContext context, Offset center, \{Animation<double> activationAnimation, Animation<double> enableAnimation, bool isDiscrete, bool isOnTop, TextPainter labelPainter, double textScaleFactor, Size sizeWithOverflow, RenderBox parentBox, SliderThemeData sliderTheme, TextDirection textDirection, double value, Thumb thumb\}) → void

Paints the value indicator shape based on the state passed to it. \[...\]

toString() → String

Returns a string representation of this object.

inherited

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/slider_theme.dart#L1165