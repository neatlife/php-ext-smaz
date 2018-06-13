# smaz Extension for PHP

smaz string algorithm write by c extensionfor php.

## Build from sources

``` bash
% git clone git@github.com:neatlife/php-ext-smaz.git
% phpize
% ./configure
% make
% make install
```

To use the system library

``` bash
% ./configure --with-smaz
```

## Configration

smaz.ini:

```
extension=smaz.so
```

## Function

* smaz\_compress — smaz string compression
* smaz\_decompress — smaz string decompression

### smaz\_compress — SMAZ compression

#### Description

string **smaz\_compress** ( string _$data_ )

SMAZ compression.

#### Pameters

* _data_

  The string to compress.

#### Return Values

Returns the compressed data or FALSE if an error occurred.


### smaz\_decompress — SMAZ decompression

#### Description

string **smaz\_decompress** ( string _$data_ )

SMAZ decompression.

> Alias: smaz\_decompress

#### Pameters

* _data_

  The compressed string.

#### Return Values

Returns the decompressed data or FALSE if an error occurred.

## Examples

```php
$data = smaz_compress('test');
smaz_decompress($data);
```
