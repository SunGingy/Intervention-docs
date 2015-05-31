# rotate — Rotate an image

## 描述

> public Intervention\Image\Image rotate(float $angle, [string $bgcolor])

Rotate the current image counter-clockwise by a given **angle**. Optionally define a **background color** for the uncovered zone after the rotation.

## 参数

### angle
The rotation angle in degrees to rotate the image counter-clockwise.

### bgcolor (optional)
A background color for the uncovered zone after the rotation. The background color can be passed in in different [color formats](/getting_started/formats). Default: ```#000000```


## 返回值
Instance of Intervention\Image\Image

## 示例

```php
// create Image from file
$img = Image::make('public/foo.jpg');

// rotate image 45 degrees clockwise
$img->rotate(-45);
```

## 参考

- [flip](/api/flip)
- [resize](/api/resize)
- [resizeCanvas](/api/resizeCanvas)
