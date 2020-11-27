[*description*][description]

# StackFit enum Null safety #

How to size the non-positioned children of a Stack.

This enum is used with Stack.fit and RenderStack.fit to control how the BoxConstraints passed from the stack's parent to the stack's child are adjusted.

See also:

 *  Stack, the widget that uses this.
 *  RenderStack, the render object that implements the stack algorithm.

## Constants ##

expand → const StackFit

The constraints passed to the stack from its parent are tightened to the biggest size allowed.

For example, if the stack has loose constraints with a width in the range 10 to 100 and a height in the range 0 to 600, then the non-positioned children of the stack would all be sized as 100 pixels wide and 600 high.

`const StackFit(1)`

loose → const StackFit

The constraints passed to the stack from its parent are loosened.

For example, if the stack has constraints that force it to 350x600, then this would allow the non-positioned children of the stack to have any width from zero to 350 and any height from zero to 600.

See also:

 *  Center, which loosens the constraints passed to its child and then centers the child in itself.
 *  BoxConstraints.loosen, which implements the loosening of box constraints.

`const StackFit(0)`

passthrough → const StackFit

The constraints passed to the stack from its parent are passed unmodified to the non-positioned children.

For example, if a Stack is an Expanded child of a Row, the horizontal constraints will be tight and the vertical constraints will be loose.

`const StackFit(2)`

values → const List<StackFit>

A constant List of the values in this enum, in order of their declaration.

`const List<StackFit>`

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/rendering/stack.dart#L239