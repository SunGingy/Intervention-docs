# interlace — Toggle interlaced mode

## 描述

> public Intervention\Image\Image interlace([boolean $interlace])

Determine whether an image should be encoded in interlaced or standard mode by toggling **interlace** mode with a boolean parameter. If an JPEG image is set interlaced the image will be processed as a progressive JPEG.


## 参数

### interlace (optional)
If interlace is set to boolean ```true``` the image will be encoded interlaced. If the parameter is set to ```false``` interlaced mode is turned off. Default: true


## 返回值
Instance of Intervention\Image\Image

## 示例

```php
// open image
$img = Image::make('public/foo.png');

// enable interlacing
$img->interlace();

// save image interlaced
$img->save();

// open interlaced image
$img = Image::make('public/interlaced.gif');

// disable interlacing
$img->interlace(false);

// save image in standard mode
$img->save();
```

## 参考

- [limitColors](/api/limitColors)
- [save](/api/save)
- [encode](/api/encde)
