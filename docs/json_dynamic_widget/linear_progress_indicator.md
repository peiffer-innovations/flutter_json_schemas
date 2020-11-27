[*description*][description]

# LinearProgressIndicator class #

A material design linear progress indicator, also known as a progress bar.

A widget that shows progress along a line. There are two kinds of linear progress indicators:

 *  *Determinate*. Determinate progress indicators have a specific value at each point in time, and the value should increase monotonically from 0.0 to 1.0, at which time the indicator is complete. To create a determinate progress indicator, use a non-null value between 0.0 and 1.0.
 *  *Indeterminate*. Indeterminate progress indicators do not have a specific value at each point in time and instead indicate that progress is being made without indicating how much progress remains. To create an indeterminate progress indicator, use a null value.

The indicator line is displayed with valueColor, an animated value. To specify a constant color value use: `AlwaysStoppedAnimation<Color>(color)`.

The minimum height of the indicator can be specified using minHeight. The indicator can be made taller by wrapping the widget with a SizedBox.

See also:

 *  CircularProgressIndicator, which shows progress along a circular arc.
 *  RefreshIndicator, which automatically displays a CircularProgressIndicator when the underlying vertical scrollable is overscrolled.
 *  [material.io/design/components/progress-indicators.html\#linear-progress-indicators][material.io_design_components_progress-indicators.html_linear-progress-indicators]

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatefulWidget
 *  ProgressIndicator
 *  LinearProgressIndicator

## Constructors ##

LinearProgressIndicator(\{Key key, double value, Color backgroundColor, Animation<Color> valueColor, double minHeight, String semanticsLabel, String semanticsValue\})

Creates a linear progress indicator. \[...\]

const

## Properties ##

backgroundColor → Color

The progress indicator's background color. \[...\]

final, inherited

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

minHeight → double

The minimum height of the line used to draw the indicator. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

semanticsLabel → String

\{@template flutter.material.progressIndicator.semanticsLabel\} The SemanticsProperties.label for this progress indicator. \[...\]

final, inherited

semanticsValue → String

\{@template flutter.material.progressIndicator.semanticsValue\} The SemanticsProperties.value for this progress indicator. \[...\]

final, inherited

value → double

If non-null, the value of this progress indicator. \[...\]

final, inherited

valueColor → Animation<Color>

The progress indicator's color as an animated value. \[...\]

final, inherited

## Methods ##

createElement() → StatefulElement

Creates a StatefulElement to manage this widget's location in the tree. \[...\]

inherited

createState() → \_LinearProgressIndicatorState

Creates the mutable state for this widget at a given location in the tree. \[...\]

override

debugDescribeChildren() → List<DiagnosticsNode>

Returns a list of DiagnosticsNode objects describing this node's children. \[...\]

@protected, inherited

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

inherited

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

toDiagnosticsNode(\{String name, DiagnosticsTreeStyle style\}) → DiagnosticsNode

Returns a debug representation of the object that is used by debugging tools and by DiagnosticsNode.toStringDeep. \[...\]

inherited

toString(\{DiagnosticLevel minLevel: DiagnosticLevel.info\}) → String

Returns a string representation of this object.

inherited

toStringDeep(\{String prefixLineOne: '', String prefixOtherLines, DiagnosticLevel minLevel: DiagnosticLevel.debug\}) → String

Returns a string representation of this node and its descendants. \[...\]

inherited

toStringShallow(\{String joiner: ', ', DiagnosticLevel minLevel: DiagnosticLevel.debug\}) → String

Returns a one-line detailed description of the object. \[...\]

inherited

toStringShort() → String

A short, textual description of this widget.

inherited

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

@nonVirtual, inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/progress_indicator.dart#L236
[material.io_design_components_progress-indicators.html_linear-progress-indicators]: https://material.io/design/components/progress-indicators.html#linear-progress-indicators