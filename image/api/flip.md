# flip — Mirror an image

## 描述

> public Intervention\Image\Image flip( [mixed $mode] )

Mirror the current image horizontally or vertically by specifying the **mode**.


## 参数

### mode (optional)
Specify the mode the image will be flipped. You can set ```h``` for horizontal (default) or ```v``` for vertical flip.


## 返回值
Instance of Intervention\Image\Image

## 示例

```php
// create Image from file
$img = Image::make('public/foo.jpg');

// flip image vertically
$img->flip('v');
```

## 参考

- [rotate](/api/rotate)
