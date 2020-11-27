[*description*][description]

# SliderComponentShape class #

Base class for slider thumb, thumb overlay, and value indicator shapes.

Create a subclass of this if you would like a custom shape.

All shapes are painted to the same canvas and ordering is important. The overlay is painted first, then the value indicator, then the thumb.

The thumb painting can be skipped by specifying noThumb for SliderThemeData.thumbShape.

The overlay painting can be skipped by specifying noOverlay for SliderThemeData.overlayShape.

See also:

 *  RoundSliderThumbShape, which is the default Slider's thumb shape that paints a solid circle.
 *  RoundSliderOverlayShape, which is the default Slider and RangeSlider's overlay shape that paints a transparent circle.
 *  PaddleSliderValueIndicatorShape, which is the default Slider's value indicator shape that paints a custom path with text in it.

Implementers

 *  PaddleSliderValueIndicatorShape
 *  RectangularSliderValueIndicatorShape
 *  RoundSliderOverlayShape
 *  RoundSliderThumbShape

## Constructors ##

SliderComponentShape()

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

Returns the preferred size of the shape, based on the given conditions.

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

paint(PaintingContext context, Offset center, \{Animation<double> activationAnimation, Animation<double> enableAnimation, bool isDiscrete, TextPainter labelPainter, RenderBox parentBox, SliderThemeData sliderTheme, TextDirection textDirection, double value, double textScaleFactor, Size sizeWithOverflow\}) → void

Paints the shape, taking into account the state passed to it. \[...\]

toString() → String

Returns a string representation of this object.

inherited

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

inherited

## Static Properties ##

noOverlay → SliderComponentShape

Special instance of SliderComponentShape to skip the overlay drawing. \[...\]

final

noThumb → SliderComponentShape

Special instance of SliderComponentShape to skip the thumb drawing. \[...\]

final


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/slider_theme.dart#L798