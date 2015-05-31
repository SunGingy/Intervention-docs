# mime — Get MIME Type

## 描述

> public Intervention\Image\Image mime()

Read MIME Type of current image instance, if it's already defined.

## 参数

none

## 返回值
MIME Type of current image.

Examples

```php
// read mime type of image
$mime = Image::make('public/foo.jpg')->mime();
```

## 参考

- [width](/api/width)
- [height](/api/height)
- [exif](/api/exif)
