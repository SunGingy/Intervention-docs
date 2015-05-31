# gamma — Apply gamma correction

## 描述

> public Intervention\Image\Image gamma( float $correction )

Performs a gamma correction operation on the current image.


## 参数

### correction
Gamma compensation value.


## 返回值
Instance of Intervention\Image\Image

## 示例

```php
// create new Intervention Image
$img = Image::make('public/foo.jpg');

// apply gamma correction
$img->gamma(1.6);
```

## 参考

- [brightness](/api/brightness)
- [contrast](/api/contrast)
- [colorize](/api/colorize)
- [greyscale](/api/greyscale)
- [invert](/api/invert)
- [pixelate](/api/pixelate)
