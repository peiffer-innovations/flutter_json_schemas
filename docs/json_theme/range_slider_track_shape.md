[*description*][description]

# RangeSliderTrackShape class #

Base class for RangeSlider track shapes.

The slider's thumbs move along the track. A discrete slider's tick marks are drawn after the track, but before the thumb, and are aligned with the track.

The getPreferredRect helps position the slider thumbs and tick marks relative to the track.

See also:

 *  RoundedRectRangeSliderTrackShape for the default RangeSlider's track shape that paints a stadium-like track.
 *  RangeSliderTickMarkShape, which can be used to create custom shapes for the RangeSlider's tick marks.
 *  RangeSliderThumbShape, which can be used to create custom shapes for the RangeSlider's thumb.
 *  RangeSliderValueIndicatorShape, which can be used to create custom shapes for the RangeSlider's value indicator.
 *  SliderComponentShape, which can be used to create custom shapes for the Slider's thumb, overlay, and value indicator and the RangeSlider's overlay.

Implementers

 *  RectangularRangeSliderTrackShape
 *  RoundedRectRangeSliderTrackShape

## Constructors ##

RangeSliderTrackShape()

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

getPreferredRect(\{RenderBox parentBox, Offset offset: Offset.zero, SliderThemeData sliderTheme, bool isEnabled, bool isDiscrete\}) → Rect

Returns the preferred bounds of the shape. \[...\]

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

paint(PaintingContext context, Offset offset, \{RenderBox parentBox, SliderThemeData sliderTheme, Animation<double> enableAnimation, Offset startThumbCenter, Offset endThumbCenter, bool isEnabled, bool isDiscrete, TextDirection textDirection\}) → void

Paints the track shape based on the state passed to it. \[...\]

toString() → String

Returns a string representation of this object.

inherited

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/slider_theme.dart#L1340