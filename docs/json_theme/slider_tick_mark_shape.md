[*description*][description]

# SliderTickMarkShape class #

Base class for Slider tick mark shapes.

Create a subclass of this if you would like a custom slider tick mark shape.

The tick mark painting can be skipped by specifying noTickMark for SliderThemeData.tickMarkShape.

See also:

 *  RoundSliderTickMarkShape, which is the default Slider's tick mark shape that paints a solid circle.
 *  SliderTrackShape, which can be used to create custom shapes for the Slider's track.
 *  SliderComponentShape, which can be used to create custom shapes for the Slider's thumb, overlay, and value indicator and the RangeSlider's overlay.

Implementers

 *  RoundSliderTickMarkShape

## Constructors ##

SliderTickMarkShape()

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

paint(PaintingContext context, Offset center, \{RenderBox parentBox, SliderThemeData sliderTheme, Animation<double> enableAnimation, Offset thumbCenter, bool isEnabled, TextDirection textDirection\}) → void

Paints the slider track. \[...\]

toString() → String

Returns a string representation of this object.

inherited

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

inherited

## Static Properties ##

noTickMark → SliderTickMarkShape

Special instance of SliderTickMarkShape to skip the tick mark painting. \[...\]

final


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/slider_theme.dart#L915