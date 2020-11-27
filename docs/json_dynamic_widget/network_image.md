[*description*][description]

# NetworkImage class Null safety #

Fetches the given URL from the network, associating it with the given scale.

The image will be cached regardless of cache headers from the server.

When a network image is used on the Web platform, the `cacheWidth` and `cacheHeight` parameters of the DecoderCallback are ignored as the Web engine delegates image decoding of network images to the Web, which does not support custom decode sizes.

See also:

 *  Image.network for a shorthand of an Image widget backed by NetworkImage.

Inheritance

 *  Object
 *  ImageProvider<NetworkImage>
 *  NetworkImage

## Constructors ##

NetworkImage(String url, \{double scale, Map<String, String>? headers\})

Creates an object that fetches the image at the given URL. \[...\]

const

factory

## Properties ##

hashCode → int

The hash code for this object. \[...\]

read-only, inherited

headers → Map<String, String>?

The HTTP headers that will be used with HttpClient.get to fetch image from network. \[...\]

read-only

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

scale → double

The scale to place in the ImageInfo object of the image.

read-only

url → String

The URL from which the image will be fetched.

read-only

## Methods ##

createStream(ImageConfiguration configuration) → ImageStream

Called by resolve to create the ImageStream it returns. \[...\]

@protected, inherited

evict(\{ImageCache? cache, ImageConfiguration configuration: ImageConfiguration.empty\}) → Future<bool>

Evicts an entry from the image cache. \[...\]

inherited

load(NetworkImage key, DecoderCallback decode) → ImageStreamCompleter

Converts a key into an ImageStreamCompleter, and begins fetching the image. \[...\]

override

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

obtainCacheStatus(\{required ImageConfiguration configuration, ImageErrorListener? handleError\}) → Future<ImageCacheStatus>

Returns the cache location for the key that this ImageProvider creates. \[...\]

inherited

obtainKey(ImageConfiguration configuration) → Future<NetworkImage>

Converts an ImageProvider's settings plus an ImageConfiguration to a key that describes the precise image to load. \[...\]

inherited

resolve(ImageConfiguration configuration) → ImageStream

Resolves this image provider using the given `configuration`, returning an ImageStream. \[...\]

@nonVirtual, inherited

resolveStreamForKey(ImageConfiguration configuration, ImageStream stream, NetworkImage key, ImageErrorListener handleError) → void

Called by resolve with the key returned by obtainKey. \[...\]

@protected, inherited

toString() → String

Returns a string representation of this object.

inherited

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/painting/image_provider.dart#L818