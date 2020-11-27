[*description*][description]

# BoxConstraints class Null safety #

Immutable layout constraints for RenderBox layout.

A Size respects a BoxConstraints if, and only if, all of the following relations hold:

 *  minWidth <= Size.width <= maxWidth
 *  minHeight <= Size.height <= maxHeight

The constraints themselves must satisfy these relations:

 *  0.0 <= minWidth <= maxWidth <= double.infinity
 *  0.0 <= minHeight <= maxHeight <= double.infinity

double.infinity is a legal value for each constraint.

## The box layout model ##

Render objects in the Flutter framework are laid out by a one-pass layout model which walks down the render tree passing constraints, then walks back up the render tree passing concrete geometry.

For boxes, the constraints are BoxConstraints, which, as described herein, consist of four numbers: a minimum width minWidth, a maximum width maxWidth, a minimum height minHeight, and a maximum height maxHeight.

The geometry for boxes consists of a Size, which must satisfy the constraints described above.

Each RenderBox (the objects that provide the layout models for box widgets) receives BoxConstraints from its parent, then lays out each of its children, then picks a Size that satisfies the BoxConstraints.

Render objects position their children independently of laying them out. Frequently, the parent will use the children's sizes to determine their position. A child does not know its position and will not necessarily be laid out again, or repainted, if its position changes.

## Terminology ##

When the minimum constraints and the maximum constraint in an axis are the same, that axis is *tightly* constrained. See: new BoxConstraints.tightFor, new BoxConstraints.tightForFinite, tighten, hasTightWidth, hasTightHeight, isTight.

An axis with a minimum constraint of 0.0 is *loose* (regardless of the maximum constraint; if it is also 0.0, then the axis is simultaneously tight and loose!). See: new BoxConstraints.loose, loosen.

An axis whose maximum constraint is not infinite is *bounded*. See: hasBoundedWidth, hasBoundedHeight.

An axis whose maximum constraint is infinite is *unbounded*. An axis is *expanding* if it is tightly infinite (its minimum and maximum constraints are both infinite). See: new BoxConstraints.expand.

An axis whose *minimum* constraint is infinite is just said to be *infinite* (since by definition the maximum constraint must also be infinite in that case). See: hasInfiniteWidth, hasInfiniteHeight.

A size is *constrained* when it satisfies a BoxConstraints description. See: constrain, constrainWidth, constrainHeight, constrainDimensions, constrainSizeAndAttemptToPreserveAspectRatio, isSatisfiedBy.

Inheritance

 *  Object
 *  Constraints
 *  BoxConstraints

## Constructors ##

BoxConstraints(\{double minWidth: 0.0, double maxWidth: double.infinity, double minHeight: 0.0, double maxHeight: double.infinity\})

Creates box constraints with the given constraints.

const

BoxConstraints.expand(\{double? width, double? height\})

Creates box constraints that expand to fill another box constraints. \[...\]

const

BoxConstraints.loose(Size size)

Creates box constraints that forbid sizes larger than the given size.

BoxConstraints.tight(Size size)

Creates box constraints that is respected only by the given size.

BoxConstraints.tightFor(\{double? width, double? height\})

Creates box constraints that require the given width or height. \[...\]

const

BoxConstraints.tightForFinite(\{double width: double.infinity, double height: double.infinity\})

Creates box constraints that require the given width or height, except if they are infinite. \[...\]

const

## Properties ##

biggest → Size

The biggest size that satisfies the constraints.

read-only

flipped → BoxConstraints

A box constraints with the width and height constraints flipped.

read-only

hasBoundedHeight → bool

Whether there is an upper bound on the maximum height. \[...\]

read-only

hasBoundedWidth → bool

Whether there is an upper bound on the maximum width. \[...\]

read-only

hashCode → int

The hash code for this object. \[...\]

read-only, override

hasInfiniteHeight → bool

Whether the height constraint is infinite. \[...\]

read-only

hasInfiniteWidth → bool

Whether the width constraint is infinite. \[...\]

read-only

hasTightHeight → bool

Whether there is exactly one height value that satisfies the constraints.

read-only

hasTightWidth → bool

Whether there is exactly one width value that satisfies the constraints.

read-only

isNormalized → bool

Returns whether the object's constraints are normalized. Constraints are normalized if the minimums are less than or equal to the corresponding maximums. \[...\]

read-only, override

isTight → bool

Whether there is exactly one size that satisfies the constraints.

read-only, override

maxHeight → double

The maximum height that satisfies the constraints. \[...\]

final

maxWidth → double

The maximum width that satisfies the constraints. \[...\]

final

minHeight → double

The minimum height that satisfies the constraints.

final

minWidth → double

The minimum width that satisfies the constraints.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

smallest → Size

The smallest size that satisfies the constraints.

read-only

## Methods ##

constrain(Size size) → Size

Returns the size that both satisfies the constraints and is as close as possible to the given size. \[...\]

constrainDimensions(double width, double height) → Size

Returns the size that both satisfies the constraints and is as close as possible to the given width and height. \[...\]

constrainHeight(\[double height = double.infinity\]) → double

Returns the height that both satisfies the constraints and is as close as possible to the given height.

constrainSizeAndAttemptToPreserveAspectRatio(Size size) → Size

Returns a size that attempts to meet the following conditions, in order: \[...\]

constrainWidth(\[double width = double.infinity\]) → double

Returns the width that both satisfies the constraints and is as close as possible to the given width.

copyWith(\{double? minWidth, double? maxWidth, double? minHeight, double? maxHeight\}) → BoxConstraints

Creates a copy of this box constraints but with the given fields replaced with the new values.

debugAssertIsValid(\{bool isAppliedConstraint: false, InformationCollector? informationCollector\}) → bool

Asserts that the constraints are valid. \[...\]

override

deflate(EdgeInsets edges) → BoxConstraints

Returns new box constraints that are smaller by the given edge dimensions.

enforce(BoxConstraints constraints) → BoxConstraints

Returns new box constraints that respect the given constraints while being as close as possible to the original constraints.

heightConstraints() → BoxConstraints

Returns box constraints with the same height constraints but with unconstrained width.

isSatisfiedBy(Size size) → bool

Whether the given size satisfies the constraints.

loosen() → BoxConstraints

Returns new box constraints that remove the minimum width and height requirements.

normalize() → BoxConstraints

Returns a box constraints that isNormalized. \[...\]

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

tighten(\{double? width, double? height\}) → BoxConstraints

Returns new box constraints with a tight width and/or height as close to the given width and height as possible while still respecting the original box constraints.

toString() → String

Returns a string representation of this object.

override

widthConstraints() → BoxConstraints

Returns box constraints with the same width constraints but with unconstrained height.

## Operators ##

operator %(double value) → BoxConstraints

Computes the remainder of each constraint parameter by the given value.

operator \*(double factor) → BoxConstraints

Scales each constraint parameter by the given factor.

operator /(double factor) → BoxConstraints

Scales each constraint parameter by the inverse of the given factor.

operator ==(Object other) → bool

The equality operator. \[...\]

override

operator ~/(double factor) → BoxConstraints

Scales each constraint parameter by the inverse of the given factor, rounded to the nearest integer.

## Static Methods ##

lerp(BoxConstraints? a, BoxConstraints? b, double t) → BoxConstraints?

Linearly interpolate between two BoxConstraints. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/rendering/box.dart#L86