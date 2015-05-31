# 调整大小 — 调整当前图片大小

## 描述
    
> public Intervention\Image\Image resize (integer $width, integer $height, [Closure $callback])

根据传入的 **宽** 和 **高** 调整当前图片的大小. 可以在第三个可选参数传入一个闭包, 来限制 `resize` 命令.

## 参数

### width 宽度
新图片的宽度

### height 高度
新图片的的高度

### callback 回调 (可选)
Closure callback defining constraints on the resize. It's possible to contraint the **aspect-ratio** and/or a unwanted **upsizing** of the image. See examples below.

#### aspectRatio

> public Intervention\Image\Size aspectRatio()

Constraint the current aspect-ratio if the image. As a shortcut to proportional resizing you can use [widen()](/api/widen) or [heighten()](/api/heighten).

#### upsize

> public Intervention\Image\Size upsize()

Keep image from being upsized.

    
## 返回值
Intervention\Image\Image 的实例对象

## 示例

```php
// create instance
$img = Image::make('public/foo.jpg')

// resize image to fixed size
$img->resize(300, 200);

// resize only the width of the image
$img->resize(300, null);

// resize only the height of the image
$img->resize(null, 200);

// resize the image to a width of 300 and constrain aspect ratio (auto height)
$img->resize(300, null, function ($constraint) {
    $constraint->aspectRatio();
});

// resize the image to a height of 200 and constrain aspect ratio (auto width)
$img->resize(null, 200, function ($constraint) {
    $constraint->aspectRatio();
});

// prevent possible upsizing
$img->resize(null, 400, function ($constraint) {
    $constraint->aspectRatio();
    $constraint->upsize();
});
```

## 参考

- [widen](/api/widen)
- [heighten](/api/heighten)
- [fit](/api/fit)
- [resizeCanvas](/api/resizeCanvas)
- [crop](/api/crop)
- [trim](/api/trim)
