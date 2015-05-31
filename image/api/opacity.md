# opacity — Set opacity of an image

## 描述

> public Intervention\Image\Image opacity( integer $transparency )

Set the **opacity** in percent of the current image ranging from 100% for opaque and 0% for full transparency.

**Note: Performance intensive on larger images. Use with care.**

## 参数

### transparency
The new percent of transparency for the current image.


## 返回值
Instance of Intervention\Image\Image

## 示例

```php
// create Image from file and set transparency to 50%
Image::make('public/foo.jpg')->opacity(50);

// create new Intervention Image from file and set image full transparent
$img = Image::make('public/foo.jpg');
$img->opacity(0);
```

## 参考

- [fill](/api/fill)
- [mask](/api/mask)
