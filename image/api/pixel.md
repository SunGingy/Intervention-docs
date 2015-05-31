# pixel — Draw a single pixel

## 描述

> public Intervention\Image\Image pixel(mixed $color, integer $x, integer $y)

Draw a single pixel in given **color** on **x, y position**.


## 参数

### color
The color of the pixel. Pass a color in one of the different [color formats](/getting_started/formats).

### x
x-coordinate of the pixel.

### y
y-coordinate of the pixel.

## 返回值
Instance of Intervention\Image\Image

## 示例

```php
// create empty canvas with background color
$img = Image::canvas(100, 100, '#ddd');

// draw a blue pixel
$img->pixel('#0000ff', 32, 32);

// draw a red pixel
$img->pixel('#ff0000', 64, 64);
```


## 参考

- [line](/api/line)
- [rectangle](/api/rectangle)
- [circle](/api/circle)
- [ellipse](/api/ellipse)
- [polygon](/api/polygon)
