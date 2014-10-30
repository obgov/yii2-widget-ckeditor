CKEditor Widget for Yii2
========================

Renders a [CKEditor WYSIWYG text editor plugin](http://www.ckeditor.com) widget.

Installation
------------
The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require "skeeks/yii2-widget-ckeditor" "*"
```
or add

```json
"skeeks/yii2-widget-ckeditor" : "*"
```

to the require section of your application's `composer.json` file.

Skins & Plugins
---------------

This widget works with default's `dev-full/stable` branch of CKEditor, with a set of plugins and skins. If you wish to
configure a different skins or plugins that the one proposed, you will have to download them separately and configure
the widget's `clientOptions` attribute accordingly.


Usage
-----
The library comes with two widgets: `CKEditor` and `CKEditorInline`. One is for classic edition and the other for inline
editing respectively.

Using a model with a basic preset:

```

use skeeks\widget\ckeditor\CKEditor;


<?= $form->field($model, 'text')->widget(CKEditor::className(), [
		'options' => ['rows' => 6],
		'preset' => 'basic'
	]) ?>
```
Using inline edition with basic preset:

```

use skeeks\widget\ckeditor\CKEditorInline;

<?php CKEditorInline::begin(['preset' => 'basic']);?>
	This text can be edited now :)
<?php CKEditorInline::end();?>
```

Further Information
-------------------
Please, check the [CKEditor plugin site](http://www.ckeditor.com) documentation for further information about its configuration options.


> [![skeeks!](https://gravatar.com/userimage/74431132/13d04d83218593564422770b616e5622.jpg)](http://www.skeeks.com)  
<i>Web development has never been so fun!</i>  
[www.skeeks.com](http://www.skeeks.com)
