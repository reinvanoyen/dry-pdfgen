# dry-pdfgen
## Generate pdf's

#### Installation
```ssh
composer require reinvanoyen/dry-pdfgen
```

#### Register the service provider
```php
<?php

$app = new \Oak\Application();

$app->register([
    \Tnt\PdfGen\PdfGenServiceProvider::class,
]);

$app->bootstrap();
```

#### Basic usage

```php
<?php

$pdfGenerator = $app->get(PdfGenerator::class);
$pdfGenerator->fromHtml('<strong>This is an example</strong>');

// Stream the pdf
$pdfGenerator->stream();
// or...
// ...use the pdf file contents
$contents = $pdfGenerator->output();
```
