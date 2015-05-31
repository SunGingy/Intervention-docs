# iptc — Reads IPTC meta data from image

## 描述

> public Intervention\Image\Image iptc([string $key])

Read IPTC meta data from current image.

## 参数

### key (optional)
Optionally index key to retrieve only particular value. By default all data available will be parsed.


## 返回值
Associative array of all meta data values available or mixed data for particular value. If no meta data can be found, method will return NULL.


## 示例

```php
// read all existing data into an array
$data = Image::make('public/foo.jpg')->iptc();

// read only 'Copyright'
$copyright = Image::make('public/foo.jpg')->iptc('Copyright');
```

## 参考

- [exif](/api/exif)
- [orientate](/api/orientate)
