blobcounter.js
=========
A blob counter library written in pure javascript.

This library helps you find blobs in an image . Inspired by BlobCounter Class in AForge.NET Framework .

## Installation

Just include the `blobcounter.js` anywhere you like :
```html
<script type="text/javascript" src="blobcounter.js"></script>
```
Or the `blobcounter.min.js`which is minified :
```html
<script type="text/javascript" src="blobcounter.min.js"></script>
```

## Usage
NOTE: Input image must be black and white. ( black blobs with white background )
```javascript
var blobs = new blobcounter(canvas); // Don't forget that input image must be all black and white ( black blobs with white background ) . Apply threshold filter to do that . 
var res = blobs.detect(1); // Radius area is one pixel . You can change it.

for (var i = 0; i < res.length; i++) {
	var cog = res[i].cog; // Center of gravity . res[i].cog.x and res[i].cog.y
	var mess = res[i].mess; // Number of pixels
}
```
See the [example.html](../master/example.html) for a practical example .

## Contributing

This library may be a poor written code as i'm not a javascript programmer so any contributing would be a huge help.
