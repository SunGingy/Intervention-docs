# sharpen — Sharpen an image

## 描述

> public Intervention\Image\Image sharpen([integer $amount])

Sharpen current image with an optional **amount**. Use values between ```0``` and ```100```.

## 参数

### amount (optional)
The amount of the sharpening strength. Method accepts values between 0 and 100. Default: 10

## 返回值
Instance of Intervention\Image\Image

Examples

```php
// create new Intervention Image
$img = Image::make('public/foo.jpg');

// sharpen image
$img->sharpen(15);
```

## 参考

- [blur](/api/blur)
