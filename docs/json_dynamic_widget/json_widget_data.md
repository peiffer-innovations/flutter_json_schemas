# JsonWidgetData class #

Inheritance

 *  [Object][]
 *  [JsonClass][]
 *  JsonWidgetData

Implementers

 *  DeferredJsonWidgetData

## Constructors ##

JsonWidgetData(\{dynamic args, @[required][] JsonWidgetBuilder builder(), JsonWidgetData child, [List][]<JsonWidgetData> children, [Set][]<[String][]> dynamicKeys, [String][] id, JsonWidgetRegistry registry, @[required][] [String][] type\})

## Properties ##

args → dynamic

final

builder → JsonWidgetBuilder Function()

final

children → [List][]<JsonWidgetData>

final

dynamicKeys → [Set][]<[String][]>

final

[hashCode][] → [int][]

The hash code for this object. [\[...\]][hashCode]

read-only, inherited

id → [String][]

final

registry → JsonWidgetRegistry

final

[runtimeType][] → [Type][]

A representation of the runtime type of the object.

read-only, inherited

type → [String][]

final

## Methods ##

build(\{[ChildWidgetBuilder][] childBuilder, [BuildContext][] context\}) → [Widget][]

Convenience method that can build the widget this data object represents. This is the equilivant of calling: `builder.build` and padding this in as the `data` parameter.

copyWith(\{dynamic args, JsonWidgetBuilder builder, [List][]<JsonWidgetData> children, [Set][]<[String][]> dynamicKeys, [String][] id, JsonWidgetRegistry registry, [String][] type\}) → JsonWidgetData

[noSuchMethod][]([Invocation][] invocation) → dynamic

Invoked when a non-existent method or property is accessed. [\[...\]][noSuchMethod]

inherited

recreate() → JsonWidgetData

Recreates the data object based on the updated values and function responces from the registry. This should only be called within the framework itself, external code should not need to call this.

toJson() → [Map][]<[String][], dynamic>

Abstract function that concrete classes must implement. This must encode the internal data model to a JSON compatible representation. \[...\]

override

[toString][]() → [String][]

Returns the string encoded JSON representation for this class. This will remove all `null` values and empty collections from the returned string.

inherited

## Operators ##

[operator ==][operator]([Object][] other) → [bool][]

The equality operator. [\[...\]][operator]

inherited

## Static Methods ##

fromDynamic(dynamic map, \{JsonWidgetRegistry registry\}) → JsonWidgetData

Decodes a JSON object into a dynamic widget. The structure is the same for all dynamic widgets with the exception of the `args` value. The `args` depends on the specific `type`. \[...\]


[Object]: https://api.dart.dev/dev/2.12.0-51.0.dev/dart-core/Object-class.html
[JsonClass]: https://pub.dev/documentation/json_class/1.0.7/json_class/JsonClass-class.html
[required]: https://pub.dev/documentation/meta/1.3.0-nullsafety.6/meta/required-constant.html
[List]: https://api.dart.dev/dev/2.12.0-51.0.dev/dart-core/List-class.html
[Set]: https://api.dart.dev/dev/2.12.0-51.0.dev/dart-core/Set-class.html
[String]: https://api.dart.dev/dev/2.12.0-51.0.dev/dart-core/String-class.html
[hashCode]: https://api.dart.dev/dev/2.12.0-51.0.dev/dart-core/Object/hashCode.html
[int]: https://api.dart.dev/dev/2.12.0-51.0.dev/dart-core/int-class.html
[runtimeType]: https://api.dart.dev/dev/2.12.0-51.0.dev/dart-core/Object/runtimeType.html
[Type]: https://api.dart.dev/dev/2.12.0-51.0.dev/dart-core/Type-class.html
[ChildWidgetBuilder]: https://pub.dev/documentation/child_builder/1.0.0+2/child_builder/ChildWidgetBuilder.html
[BuildContext]: https://api.flutter.dev/flutter/widgets/BuildContext-class.html
[Widget]: https://api.flutter.dev/flutter/widgets/Widget-class.html
[noSuchMethod]: https://api.dart.dev/dev/2.12.0-51.0.dev/dart-core/Object/noSuchMethod.html
[Invocation]: https://api.dart.dev/dev/2.12.0-51.0.dev/dart-core/Invocation-class.html
[Map]: https://api.dart.dev/dev/2.12.0-51.0.dev/dart-core/Map-class.html
[toString]: https://pub.dev/documentation/json_class/1.0.7/json_class/JsonClass/toString.html
[operator]: https://api.dart.dev/dev/2.12.0-51.0.dev/dart-core/Object/operator_equals.html
[bool]: https://api.dart.dev/dev/2.12.0-51.0.dev/dart-core/bool-class.html