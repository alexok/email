email
=====

Yii mail extension

Configure
-----

```php
'components'=>array(
    'email'=>array(
        'class'=>'application.extensions.email.Email',
        'delivery'=>'php', //Will use the php mailing function.
        //May also be set to 'debug' to instead dump the contents of the email into the view
    ),
...
```

Example code:
-----
```php
$email = Yii::app()->email;
$email->to = 'admin@example.com';
$email->subject = 'Hello';
$email->message = 'Hello brother';
$email->send();
```

Debug widget:
-----

```php
<?php $this->widget('application.extensions.email.debug'); ?>
```
