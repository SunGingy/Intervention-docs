# orientate — adjusts image orientation automatically

## 描述

> public Intervention\Image\Image orientate()

This method reads the EXIF image profile setting 'Orientation' and performs a rotation on the image to display the image correctly.

**Note: PHP must be compiled in with ```--enable-exif``` to use this method. Windows users must also have the ```mbstring``` extension enabled.**

## 参数

None

## 返回值
Instance of Intervention\Image\Image

## 示例

```php
// instantiate image with auto-orientation
$img = Image::make('foo.jpg')->orientate();
```

## 参考

- [exif](/api/exif)
