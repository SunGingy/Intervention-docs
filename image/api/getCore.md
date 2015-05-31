# getCore — Read core instance of image

## 描述

> public Intervention\Image\Image getCore()

Returns the current image in core format of the particular driver. If you're using GD, you will get the the current **GD resource** as return value. If you have setup the Imagick driver, the method will return the current image information as an **Imagick object**.

## 参数

none

## 返回值
mixed - depends on configured driver

## 示例

```php
// create Intervention Image
$img = Image::make('public/foo.jpg');

// get Imagick instance
$imagick = $img->getCore();

// apply Imagick function
$imagick->embossImage(0, 1);
```
