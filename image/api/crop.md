# crop — Crop an image

## 描述

> public Intervention\Image\Image crop(int $width, int $height, [int $x, int $y])

Cut out a rectangular part of the current image with given **width and height**. Define optional **x,y coordinates** to move the top-left corner of the cutout to a certain position.


## 参数

### width
Width of the rectangular cutout.

### height
Height of the rectangular cutout.

### x (optional)
X-Coordinate of the top-left corner if the rectangular cutout. By default the rectangular part will be centered on the current image.

### y (optional)
Y-Coordinate of the top-left corner if the rectangular cutout. By default the rectangular part will be centered on the current image.

## 返回值
Instance of Intervention\Image\Image

## 示例

```php
// open file a image resource
$img = Image::make('public/foo.jpg');

// crop image
$img->crop(100, 100, 25, 25);
```


## 参考

- [resize](/api/resize)
- [resizeCanvas](/api/resizeCanvas)
- [fit](/api/fit)
- [trim](/api/trim)
