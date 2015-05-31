# 模糊 — 对图片进行模糊操作

## 描述

> public Intervention\Image\Image blur( [integer $amount] )

应用高斯模糊滤镜到当前图片. 参数取值范围 ```0``` 到 ```100```.

**提示: 性能模糊性的应用请慎重使用 GD 库.**

## 参数

### amount (可选)
模糊的强度, 取值范围 0 到 100. 默认 1

## 返回值
Intervention\Image\Image 的实例对象

## 示例

```php
// 初始化 Intervention Image
$img = Image::make('public/foo.jpg');

// 应用轻度滤镜
$img->blur();

// 应用强度滤镜
$img->blur(15);
```

## 参考链接

- [锐化](/api/sharpen)
- [滤镜](/api/pixelate)
- [亮度](/api/brightness)
- [对比度](/api/contrast)
