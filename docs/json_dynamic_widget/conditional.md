# JsonConditionalBuilder class #

Builder that builds either the actual child widget or clears the child widgets based on the result from the conditional.

See the fromDynamic for the format.

Inheritance

 *  [Object][]
 *  JsonWidgetBuilder
 *  JsonConditionalBuilder

## Constructors ##

JsonConditionalBuilder(\{@[required][] [Conditional][] conditional, @[required][] [Set][]<[String][]> keys, JsonWidgetData onFalse\})

## Properties ##

conditional → [Conditional][]

final

[hashCode][] → [int][]

The hash code for this object. [\[...\]][hashCode]

read-only, inherited

keys → [Set][]<[String][]>

final

onFalse → JsonWidgetData

final

preferredSizeWidget → [bool][]

final, inherited

[runtimeType][] → [Type][]

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

build(\{[ChildWidgetBuilder][] childBuilder, [BuildContext][] context, JsonWidgetData data\}) → [Widget][]

Builds the widget. If there are dynamic keys on the `data` object, and the widget is not a [PreferredSizeWidget][], then the returned widget will be wrapped by a stateful widget that will rebuild if any of the dynamic args change in value.

@[nonVirtual][], inherited

buildCustom(\{[ChildWidgetBuilder][] childBuilder, [BuildContext][] context, JsonWidgetData data, [Key][] key\}) → [Widget][]

Custom builder that subclasses must override and implement to return the actual [Widget][] to be placed on the tree.

override

[noSuchMethod][]([Invocation][] invocation) → dynamic

Invoked when a non-existent method or property is accessed. [\[...\]][noSuchMethod]

inherited

remove(JsonWidgetData data) → void

Called when a JSON widget is removed from the tree due to a conditional. Custom widgets may need to implement this to clean up values that may have been placed on the JsonWidgetRegistry by the widget. \[...\]

@[mustCallSuper][], inherited

[toString][]() → [String][]

Returns a string representation of this object.

inherited

## Operators ##

[operator ==][operator]([Object][] other) → [bool][]

The equality operator. [\[...\]][operator]

inherited

## Static Methods ##

fromDynamic(dynamic map, \{JsonWidgetRegistry registry\}) → JsonConditionalBuilder

Builds the builder from a Map-like dynamic structure. This expects the JSON format to be of the following structure: \[...\]

## Constants ##

type → const [String][]

`'conditional'`


[Object]: https://api.dart.dev/dev/2.12.0-51.0.dev/dart-core/Object-class.html
[required]: https://pub.dev/documentation/meta/1.3.0-nullsafety.6/meta/required-constant.html
[Conditional]: https://pub.dev/documentation/json_conditional/1.0.3+1/json_conditional/Conditional-class.html
[Set]: https://api.dart.dev/dev/2.12.0-51.0.dev/dart-core/Set-class.html
[String]: https://api.dart.dev/dev/2.12.0-51.0.dev/dart-core/String-class.html
[hashCode]: https://api.dart.dev/dev/2.12.0-51.0.dev/dart-core/Object/hashCode.html
[int]: https://api.dart.dev/dev/2.12.0-51.0.dev/dart-core/int-class.html
[bool]: https://api.dart.dev/dev/2.12.0-51.0.dev/dart-core/bool-class.html
[runtimeType]: https://api.dart.dev/dev/2.12.0-51.0.dev/dart-core/Object/runtimeType.html
[Type]: https://api.dart.dev/dev/2.12.0-51.0.dev/dart-core/Type-class.html
[ChildWidgetBuilder]: https://pub.dev/documentation/child_builder/1.0.0+2/child_builder/ChildWidgetBuilder.html
[BuildContext]: https://api.flutter.dev/flutter/widgets/BuildContext-class.html
[Widget]: https://api.flutter.dev/flutter/widgets/Widget-class.html
[PreferredSizeWidget]: https://api.flutter.dev/flutter/widgets/PreferredSizeWidget-class.html
[nonVirtual]: https://pub.dev/documentation/meta/1.3.0-nullsafety.6/meta/nonVirtual-constant.html
[Key]: https://api.flutter.dev/flutter/foundation/Key-class.html
[noSuchMethod]: https://api.dart.dev/dev/2.12.0-51.0.dev/dart-core/Object/noSuchMethod.html
[Invocation]: https://api.dart.dev/dev/2.12.0-51.0.dev/dart-core/Invocation-class.html
[mustCallSuper]: https://pub.dev/documentation/meta/1.3.0-nullsafety.6/meta/mustCallSuper-constant.html
[toString]: https://api.dart.dev/dev/2.12.0-51.0.dev/dart-core/Object/toString.html
[operator]: https://api.dart.dev/dev/2.12.0-51.0.dev/dart-core/Object/operator_equals.html