# invert — Invert colors of an image

## 描述

> public Intervention\Image\Image invert()

Reverses all colors of the current image.


## 参数

none


## 返回值
Instance of Intervention\Image\Image

## 示例

```php
// create Image from file and reverse colors
$img = Image::make('public/foo.jpg')->invert();
```

## 参考

- [brightness](/api/brightness)
- [contrast](/api/contrast)

