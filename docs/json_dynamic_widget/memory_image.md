[*description*][description]

# MemoryImage class Null safety #

Decodes the given Uint8List buffer as an image, associating it with the given scale.

The provided bytes buffer should not be changed after it is provided to a MemoryImage. To provide an ImageStream that represents an image that changes over time, consider creating a new subclass of ImageProvider whose load method returns a subclass of ImageStreamCompleter that can handle providing multiple images.

See also:

 *  Image.memory for a shorthand of an Image widget backed by MemoryImage.

Inheritance

 *  Object
 *  ImageProvider<MemoryImage>
 *  MemoryImage

Annotations

 *  @immutable

## Constructors ##

MemoryImage(Uint8List bytes, \{double scale: 1.0\})

Creates an object that decodes a Uint8List buffer as an image. \[...\]

const

## Properties ##

bytes → Uint8List

The bytes to decode into an image.

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

scale → double

The scale to place in the ImageInfo object of the image.

final

## Methods ##

createStream(ImageConfiguration configuration) → ImageStream

Called by resolve to create the ImageStream it returns. \[...\]

@protected, inherited

evict(\{ImageCache? cache, ImageConfiguration configuration: ImageConfiguration.empty\}) → Future<bool>

Evicts an entry from the image cache. \[...\]

inherited

load(MemoryImage key, DecoderCallback decode) → ImageStreamCompleter

Converts a key into an ImageStreamCompleter, and begins fetching the image. \[...\]

override

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

obtainCacheStatus(\{required ImageConfiguration configuration, ImageErrorListener? handleError\}) → Future<ImageCacheStatus>

Returns the cache location for the key that this ImageProvider creates. \[...\]

inherited

obtainKey(ImageConfiguration configuration) → Future<MemoryImage>

Converts an ImageProvider's settings plus an ImageConfiguration to a key that describes the precise image to load. \[...\]

override

resolve(ImageConfiguration configuration) → ImageStream

Resolves this image provider using the given `configuration`, returning an ImageStream. \[...\]

@nonVirtual, inherited

resolveStreamForKey(ImageConfiguration configuration, ImageStream stream, MemoryImage key, ImageErrorListener handleError) → void

Called by resolve with the key returned by obtainKey. \[...\]

@protected, inherited

toString() → String

Returns a string representation of this object.

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

override


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/painting/image_provider.dart#L923