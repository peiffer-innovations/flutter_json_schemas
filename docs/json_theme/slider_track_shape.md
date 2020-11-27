[*description*][description]

# SliderTrackShape class #

Base class for slider track shapes.

The slider's thumb moves along the track. A discrete slider's tick marks are drawn after the track, but before the thumb, and are aligned with the track.

The getPreferredRect helps position the slider thumb and tick marks relative to the track.

See also:

 *  RoundedRectSliderTrackShape for the default Slider's track shape that paints a stadium-like track.
 *  SliderTickMarkShape, which can be used to create custom shapes for the Slider's tick marks.
 *  SliderComponentShape, which can be used to create custom shapes for the Slider's thumb, overlay, and value indicator and the RangeSlider's overlay.

Implementers

 *  RectangularSliderTrackShape
 *  RoundedRectSliderTrackShape

## Constructors ##

SliderTrackShape()

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

paint(PaintingContext context, Offset offset, \{RenderBox parentBox, SliderThemeData sliderTheme, Animation<double> enableAnimation, Offset thumbCenter, bool isEnabled, bool isDiscrete, TextDirection textDirection\}) → void

Paints the track shape based on the state passed to it. \[...\]

toString() → String

Returns a string representation of this object.

inherited

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/slider_theme.dart#L991