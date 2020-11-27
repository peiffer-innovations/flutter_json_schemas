[*description*][description]

# BoxFit enum Null safety #

How a box should be inscribed into another box.

See also:

 *  applyBoxFit, which applies the sizing semantics of these values (though not the alignment semantics).

## Constants ##

contain → const BoxFit

As large as possible while still containing the source entirely within the target box.

![box_fit_contain.png][]

`const BoxFit(1)`

cover → const BoxFit

As small as possible while still covering the entire target box.

![box_fit_cover.png][]

`const BoxFit(2)`

fill → const BoxFit

Fill the target box by distorting the source's aspect ratio.

![box_fit_fill.png][]

`const BoxFit(0)`

fitHeight → const BoxFit

Make sure the full height of the source is shown, regardless of whether this means the source overflows the target box horizontally.

![box_fit_fitHeight.png][]

`const BoxFit(4)`

fitWidth → const BoxFit

Make sure the full width of the source is shown, regardless of whether this means the source overflows the target box vertically.

![box_fit_fitWidth.png][]

`const BoxFit(3)`

none → const BoxFit

Align the source within the target box (by default, centering) and discard any portions of the source that lie outside the box.

The source image is not resized.

![box_fit_none.png][]

`const BoxFit(5)`

scaleDown → const BoxFit

Align the source within the target box (by default, centering) and, if necessary, scale the source down to ensure that the source fits within the box.

This is the same as `contain` if that would shrink the image, otherwise it is the same as `none`.

![box_fit_scaleDown.png][]

`const BoxFit(6)`

values → const List<BoxFit>

A constant List of the values in this enum, in order of their declaration.

`const List<BoxFit>`

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/painting/box_fit.dart#L18
[box_fit_contain.png]: https://flutter.github.io/assets-for-api-docs/assets/painting/box_fit_contain.png
[box_fit_cover.png]: https://flutter.github.io/assets-for-api-docs/assets/painting/box_fit_cover.png
[box_fit_fill.png]: https://flutter.github.io/assets-for-api-docs/assets/painting/box_fit_fill.png
[box_fit_fitHeight.png]: https://flutter.github.io/assets-for-api-docs/assets/painting/box_fit_fitHeight.png
[box_fit_fitWidth.png]: https://flutter.github.io/assets-for-api-docs/assets/painting/box_fit_fitWidth.png
[box_fit_none.png]: https://flutter.github.io/assets-for-api-docs/assets/painting/box_fit_none.png
[box_fit_scaleDown.png]: https://flutter.github.io/assets-for-api-docs/assets/painting/box_fit_scaleDown.png