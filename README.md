# Customize Your Main Upload Directory for Lumen Laravel

## Require
###### install properly these library

> https://github.com/thephpleague/flysystem
> https://github.com/irazasyed/larasupport

## then, download config folder above

Custom this line, to change your directory setting

> 'default' => env('FILESYSTEM_DRIVER', 'public'),

change **public** to anything you wants, related to the **object title** that you write in this code below:

> 'disks' => [
>
>        'local' => [
>            'driver' => 'local',
>            'root' => storage_path('app'),
>        ],
>
>        'public' => [
>            'driver' => 'local',
>            'root' => public_path('storage/'),
>           'url' => env('APP_URL') . '/storage',
>           'visibility' => 'public',
>       ],

if you want to change the directory to another folder, then change in the **root** line, to something like

> app_path() // app folder
> public_path() // public folder
> config_path() // config folder

Of course the recommended one is public folder, because there is the place that everyone can access, include your users.

Hope this little tutorial helps.

Thanks
