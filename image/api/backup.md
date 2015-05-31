# backup — backups current image state

## 描述

> public Intervention\Image\Image backup( [string $name] )

Backups current image state as fallback for [reset method](/api/reset) under an optional **name**. Overwrites older state on every call, unless a different name is passed.


## 参数

### name (optional)
The name of the backup in memory. Default: *default*

## 返回值
Instance of Intervention\Image\Image

## 示例

```php
// create empty canvas with black background
$img = Image::canvas(120, 90, '#000000');

// fill image with color
$img->fill('#b53717');

// backup image with colored background
$img->backup();

// fill image with tiled image
$img->fill('tile.png');

// return to colored background
$img->reset();
```

## 参考

- [reset](/api/reset)
