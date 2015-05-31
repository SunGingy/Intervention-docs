# 两顿 — 调整图片的亮度

## 描述

> public Intervention\Image\Image brightness( integer $level )

Changes the brightness of the current image by the given **level**. Use values between ```-100``` for min. brightness ```0``` for no change and ```+100``` for max. brightness.


## 参数

### level
Level of brightness change applied to the current image. Use values between -100 and +100.

## 返回值
Instance of Intervention\Image\Image

## 示例

```php
// create new Intervention Image
$img = Image::make('public/foo.jpg');

// increase brightness of image
$img->brightness(35);
```

## 参考

- [contrast](/api/contrast)
- [gamma](/api/gamma)
- [colorize](/api/colorize)
- [greyscale](/api/greyscale)
- [invert](/api/invert)
- [pixelate](/api/pixelate)
