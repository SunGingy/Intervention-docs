# heighten — Resize image proportionally to given height

## 描述

> public Intervention\Image\Image heighten(integer $height, [Closure $callback])

Resizes the current image to new **height**, constraining aspect ratio. Pass an optional Closure **callback** as third parameter, to apply additional constraints like preventing possible upsizing.

## 参数

### height
The new height of the image

### callback (optional)
Closure callback defining constraint to prevent unwanted **upsizing** of the image. See examples below.

#### upsize

> public Intervention\Image\Size upsize()

Keep image from being upsized.



## 返回值
Resized instance of Intervention\Image\Image

## 示例

```php
// resize image to new height
$img = Image::make('public/foo.jpg')->heighten(100);

// resize image to new height but do not exceed original size
$img = Image::make('public/foo.jpg')->heighten(100, function ($constraint) {
    $constraint->upsize();
});
```

## 参考

- [widen](/api/widen)
- [resize](/api/resize)
