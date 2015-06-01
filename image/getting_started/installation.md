# 安装

## 环境要求

Intervention Image 需要满足以下条件才能正常运行.

- PHP >= 5.3
- Fileinfo 扩展

和下面 **其中一个** 的图形处理库.

- GD 库 (>=2.0) &hellip; **or** &hellip;
- Imagick PHP 扩展 (>=6.5.7)

---

## 使用 Composer 安装

最好最快的安装方式是用使用 [Composer](http://getcomposer.org/).

要安装最新版本, 只需要运行以下命令:

> $ php composer.phar require intervention/image

现在你的 ```composer.json``` 文件应该已经自动更新了, 然后你可以通过仅仅引入 ```vendor/autoload.php```  这个文件来运行这个库.

后面的步骤是可选的, 如果你想在 **Laravel framework** 下完整的使用 Intervention Image. 如果你想在在 Laravel下使用这个库, 你可以跳过下面的步骤, 直接跳到 [Laravel 集成](#laravel).


---


## 使用

Intervention Image doesn't require Laravel or any other framework at all. If you want to use it as is, you just have to require the composer autoload file to instatiate image objects as shown in the following example.

#### 示例

```php
// include composer autoload
require 'vendor/autoload.php';

// import the Intervention Image Manager Class
use Intervention\Image\ImageManager;

// create an image manager instance with favored driver
$manager = new ImageManager(array('driver' => 'imagick'));

// to finally create image instances
$image = $manager->make('public/foo.jpg')->resize(300, 200);
```

You might also use the static version of ImageManager as shown in the example below.

#### 精通调用示例

```php
// include composer autoload
require 'vendor/autoload.php';

// import the Intervention Image Manager Class
use Intervention\Image\ImageManagerStatic as Image;

// configure with favored image driver (gd by default)
Image::configure(array('driver' => 'imagick'));

// and you are ready to go ...
$image = Image::make('public/foo.jpg')->resize(300, 200);
```


---


<a name="laravel"></a>
## 集成到 Laravel 

Intervention Image has optional support for [Laravel](http://laravel.com) and comes with a **Service Provider and Facades** for easy integration. The `vendor/autoload.php` is included by Laravel, so you don't have to require or autoload manually. Just see the instructions below.

After you have installed Intervention Image, open your Laravel config file ```config/app.php``` and add the following lines.

In the ```$providers``` array add the service providers for this package.

> 'Intervention\Image\ImageServiceProvider'

Add the facade of this package to the ```$aliases``` array.

> 'Image' => 'Intervention\Image\Facades\Image'

Now the Image Class will be auto-loaded by Laravel.


### 配置

By default Intervention Image uses PHP's GD library extension to process all images. If you want to switch to Imagick, you can pull a configuration file into your application by running on of the following artisan command.

#### 在 Laravel 5 下 Publish 配置 

> $ php artisan vendor:publish --provider="Intervention\Image\ImageServiceProviderLaravel5"


#### 在 Laravel 4 下 Publish 配置 

> $ php artisan config:publish intervention/image

In Laravel 5 applications the configuration file is copied to ```config/image.php```, in older Laravel 4 applications you will find the file at ```app/config/packages/intervention/image/config.php```. With this copy you can alter the image driver settings for you application locally.

#### 示例

```php
// 在 Laravel 路由下使用
Route::get('/', function()
{
    $img = Image::make('foo.jpg')->resize(300, 200);

    return $img->response('jpg');
});
```


