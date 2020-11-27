[*description*][description]

# SliderThemeData class #

Holds the color, shape, and typography values for a material design slider theme.

Use this class to configure a SliderTheme widget, or to set the ThemeData.sliderTheme for a Theme widget.

To obtain the current ambient slider theme, use SliderTheme.of.

This theme is for both the Slider and the RangeSlider. The properties that are only for the Slider are: tickMarkShape, thumbShape, trackShape, and valueIndicatorShape. The properties that are only for the RangeSlider are rangeTickMarkShape, rangeThumbShape, rangeTrackShape, rangeValueIndicatorShape, overlappingShapeStrokeColor, minThumbSeparation, and thumbSelector. All other properties are used by both the Slider and the RangeSlider.

The parts of a slider are:

 *  The "thumb", which is a shape that slides horizontally when the user drags it.
 *  The "track", which is the line that the slider thumb slides along.
 *  The "tick marks", which are regularly spaced marks that are drawn when using discrete divisions.
 *  The "value indicator", which appears when the user is dragging the thumb to indicate the value being selected.
 *  The "overlay", which appears around the thumb, and is shown when the thumb is pressed, focused, or hovered. It is painted underneath the thumb, so it must extend beyond the bounds of the thumb itself to actually be visible.
 *  The "active" side of the slider is the side between the thumb and the minimum value.
 *  The "inactive" side of the slider is the side between the thumb and the maximum value.
 *  The Slider is disabled when it is not accepting user input. See Slider for details on when this happens.

The thumb, track, tick marks, value indicator, and overlay can be customized by creating subclasses of SliderTrackShape, SliderComponentShape, and/or SliderTickMarkShape. See RoundSliderThumbShape, RectangularSliderTrackShape, RoundSliderTickMarkShape, RectangularSliderValueIndicatorShape, and RoundSliderOverlayShape for examples.

The track painting can be skipped by specifying 0 for trackHeight. The thumb painting can be skipped by specifying SliderComponentShape.noThumb for SliderThemeData.thumbShape. The overlay painting can be skipped by specifying SliderComponentShape.noOverlay for SliderThemeData.overlayShape. The tick mark painting can be skipped by specifying SliderTickMarkShape.noTickMark for SliderThemeData.tickMarkShape. The value indicator painting can be skipped by specifying the appropriate ShowValueIndicator for SliderThemeData.showValueIndicator.

See also:

 *  SliderTheme widget, which can override the slider theme of its children.
 *  Theme widget, which performs a similar function to SliderTheme, but for overall themes.
 *  ThemeData, which has a default SliderThemeData.
 *  SliderComponentShape, which can be used to create custom shapes for the Slider's thumb, overlay, and value indicator and the RangeSlider's overlay.
 *  SliderTrackShape, which can be used to create custom shapes for the Slider's track.
 *  SliderTickMarkShape, which can be used to create custom shapes for the Slider's tick marks.
 *  RangeSliderThumbShape, which can be used to create custom shapes for the RangeSlider's thumb.
 *  RangeSliderValueIndicatorShape, which can be used to create custom shapes for the RangeSlider's value indicator.
 *  RangeSliderTrackShape, which can be used to create custom shapes for the RangeSlider's track.
 *  RangeSliderTickMarkShape, which can be used to create custom shapes for the RangeSlider's tick marks.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

SliderThemeData(\{double trackHeight, Color activeTrackColor, Color inactiveTrackColor, Color disabledActiveTrackColor, Color disabledInactiveTrackColor, Color activeTickMarkColor, Color inactiveTickMarkColor, Color disabledActiveTickMarkColor, Color disabledInactiveTickMarkColor, Color thumbColor, Color overlappingShapeStrokeColor, Color disabledThumbColor, Color overlayColor, Color valueIndicatorColor, SliderComponentShape overlayShape, SliderTickMarkShape tickMarkShape, SliderComponentShape thumbShape, SliderTrackShape trackShape, SliderComponentShape valueIndicatorShape, RangeSliderTickMarkShape rangeTickMarkShape, RangeSliderThumbShape rangeThumbShape, RangeSliderTrackShape rangeTrackShape, RangeSliderValueIndicatorShape rangeValueIndicatorShape, ShowValueIndicator showValueIndicator, TextStyle valueIndicatorTextStyle, double minThumbSeparation, RangeThumbSelector thumbSelector\})

Create a SliderThemeData given a set of exact values. \[...\]

const

SliderThemeData.fromPrimaryColors(\{@required Color primaryColor, @required Color primaryColorDark, @required Color primaryColorLight, @required TextStyle valueIndicatorTextStyle\})

Generates a SliderThemeData from three main colors. \[...\]

factory

## Properties ##

activeTickMarkColor → Color

The color of the track's tick marks that are drawn between the Slider.min position and the current thumb position.

final

activeTrackColor → Color

The color of the Slider track between the Slider.min position and the current thumb position.

final

disabledActiveTickMarkColor → Color

The color of the track's tick marks that are drawn between the Slider.min position and the current thumb position when the Slider is disabled.

final

disabledActiveTrackColor → Color

The color of the Slider track between the Slider.min position and the current thumb position when the Slider is disabled.

final

disabledInactiveTickMarkColor → Color

The color of the track's tick marks that are drawn between the current thumb position and the Slider.max position when the Slider is disabled.

final

disabledInactiveTrackColor → Color

The color of the Slider track between the current thumb position and the Slider.max position when the Slider is disabled.

final

disabledThumbColor → Color

The color given to the thumbShape to draw itself with when the Slider is disabled.

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

inactiveTickMarkColor → Color

The color of the track's tick marks that are drawn between the current thumb position and the Slider.max position.

final

inactiveTrackColor → Color

The color of the Slider track between the current thumb position and the Slider.max position.

final

minThumbSeparation → double

Limits the thumb's separation distance. \[...\]

final

overlappingShapeStrokeColor → Color

The color given to the perimeter of the top rangeThumbShape when the thumbs are overlapping and the top rangeValueIndicatorShape when the value indicators are overlapping.

final

overlayColor → Color

The color of the overlay drawn around the slider thumb when it is pressed, focused, or hovered. \[...\]

final

overlayShape → SliderComponentShape

The shape that will be used to draw the Slider's overlay. \[...\]

final

rangeThumbShape → RangeSliderThumbShape

The shape that will be used for the RangeSlider's thumbs. \[...\]

final

rangeTickMarkShape → RangeSliderTickMarkShape

The shape that will be used to draw the RangeSlider's tick marks. \[...\]

final

rangeTrackShape → RangeSliderTrackShape

The shape that will be used to draw the RangeSlider's track. \[...\]

final

rangeValueIndicatorShape → RangeSliderValueIndicatorShape

The shape that will be used for the RangeSlider's value indicators. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

showValueIndicator → ShowValueIndicator

Whether the value indicator should be shown for different types of sliders. \[...\]

final

thumbColor → Color

The color given to the thumbShape to draw itself with.

final

thumbSelector → RangeThumbSelector

Determines which thumb should be selected when the slider is interacted with. \[...\]

final

thumbShape → SliderComponentShape

The shape that will be used to draw the Slider's thumb. \[...\]

final

tickMarkShape → SliderTickMarkShape

The shape that will be used to draw the Slider's tick marks. \[...\]

final

trackHeight → double

The height of the Slider track.

final

trackShape → SliderTrackShape

The shape that will be used to draw the Slider's track. \[...\]

final

valueIndicatorColor → Color

The color given to the valueIndicatorShape to draw itself with.

final

valueIndicatorShape → SliderComponentShape

The shape that will be used to draw the Slider's value indicator. \[...\]

final

valueIndicatorTextStyle → TextStyle

The text style for the text on the value indicator.

final

## Methods ##

copyWith(\{double trackHeight, Color activeTrackColor, Color inactiveTrackColor, Color disabledActiveTrackColor, Color disabledInactiveTrackColor, Color activeTickMarkColor, Color inactiveTickMarkColor, Color disabledActiveTickMarkColor, Color disabledInactiveTickMarkColor, Color thumbColor, Color overlappingShapeStrokeColor, Color disabledThumbColor, Color overlayColor, Color valueIndicatorColor, SliderComponentShape overlayShape, SliderTickMarkShape tickMarkShape, SliderComponentShape thumbShape, SliderTrackShape trackShape, SliderComponentShape valueIndicatorShape, RangeSliderTickMarkShape rangeTickMarkShape, RangeSliderThumbShape rangeThumbShape, RangeSliderTrackShape rangeTrackShape, RangeSliderValueIndicatorShape rangeValueIndicatorShape, ShowValueIndicator showValueIndicator, TextStyle valueIndicatorTextStyle, double minThumbSeparation, RangeThumbSelector thumbSelector\}) → SliderThemeData

Creates a copy of this object but with the given fields replaced with the new values.

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

lerp(SliderThemeData a, SliderThemeData b, double t) → SliderThemeData

Linearly interpolate between two slider themes. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/slider_theme.dart#L237