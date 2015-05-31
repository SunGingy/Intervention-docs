# exif — Reads Exif data from image

## 描述

> public Intervention\Image\Image exif([string $key])

Read Exif meta data from current image. Image object must be instantiated from file path.

**Note: PHP must be compiled in with ```--enable-exif``` to use this method. Windows users must also have the ```mbstring``` extension enabled.**

## 参数

### key (optional)
Optionally index key to retrieve only particular data. By default all data available will be loaded.


## 返回值
Associative array of all Exif data available or mixed data for particular value. If no meta data can be found, method will return NULL.

## 示例

```php
// read all existing data into an array
$data = Image::make('public/foo.jpg')->exif();

// read model of the camera
$name = Image::make('public/foo.jpg')->exif('Model');
```

## 参考

- [iptc](/api/iptc)
- [orientate](/api/orientate)
