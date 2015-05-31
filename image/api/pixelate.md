# pixelate — Pixelate an image

## 描述

> public Intervention\Image\Image pixelate(integer $size)

Applies a pixelation effect to the current image with a given **size** of pixels.

## 参数

### size
Size of the pixels.

## 返回值
Instance of Intervention\Image\Image

## 示例

```php
// create new Intervention Image
$img = Image::make('public/foo.jpg');

// apply pixelation effect
$img->pixelate(12);
```

## 参考

- [brightness](/api/brightness)
- [contrast](/api/contrast)
- [greyscale](/api/greyscale)
- [invert](/api/invert)
