# Install antigate client as submodule
```bash
cd /path/to/project
git submodule add git://github.com/s-larionov/yii-antigate.git protected/extensions/antigate
```

# Configure Antigate client
add to application config settings for component:
```php
return array(
    // ...
    'commonents' => array(
        // ...
        'antigate' => array(
            'class' => 'ext.antigate.EAntigateClient',
            'apiKey' => '12345678901234567890',
        ),
        // ...
    ),
    // ...
);
```

# Use client
```php
echo Yii::app()->antigate->recognizeByUrl('http://....');
```
