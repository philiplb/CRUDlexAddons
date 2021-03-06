CRUDlex Amazon S3 FileProcessor
===============================

This is a FileProcessor for [CRUDlex](https://github.com/philiplb/CRUDlex)
handling the uploaded files via Amazon S3 in CRUDlex versions not using
Flysystem for the file handling: >= 0.10.0 and <= 0.11.0.

## How To: Amazon S3 FileProcessor

First, create an instance of the Amazon S3 FileProcessor:

```php
$fileProcessor = new CRUDlex\AmazonS3FileProcessor(
    'yourRegion',
    'yourBucket',
    'yourAccessKey',
    'yourSecretAccessKey'
);
```

And then hand it in when registering the CRUDlex ServiceProvider:

```php
$app->register(new CRUDlex\ServiceProvider(), array(
    'crud.file' => __DIR__ . '<yourCrud.yml>',
    'crud.datafactory' => $dataFactory,
    'crud.fileprocessor' => $fileProcessor
));
```

## Package

[![Total Downloads](https://poser.pugx.org/philiplb/crudlexamazons3fileprocessor/downloads.svg)](https://packagist.org/packages/philiplb/crudlexamazons3fileprocessor)
[![Latest Stable Version](https://poser.pugx.org/philiplb/crudlexamazons3fileprocessor/v/stable.svg)](https://packagist.org/packages/philiplb/crudlexamazons3fileprocessor)
[![Latest Unstable Version](https://poser.pugx.org/philiplb/crudlexamazons3fileprocessor/v/unstable.svg)](https://packagist.org/packages/philiplb/crudlexamazons3fileprocessor) [![License](https://poser.pugx.org/philiplb/crudlexamazons3fileprocessor/license.svg)](https://packagist.org/packages/philiplb/crudlexamazons3fileprocessor)

### Stable

```json
"require": {
    "philiplb/crudlexamazons3fileprocessor": "0.11.0"
}
```

### Bleeding Edge

```json
"require": {
    "philiplb/crudlexamazons3fileprocessor": "0.12.x-dev"
}
```
