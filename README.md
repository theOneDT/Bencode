# PHP Bencode Library
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/14bb9525a5a343079e45d9501dac1b4c)](https://app.codacy.com/manual/rhilipruan/Bencode?utm_source=github.com&utm_medium=referral&utm_content=Rhilip/Bencode&utm_campaign=Badge_Grade_Dashboard)
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FRhilip%2FBencode.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2FRhilip%2FBencode?ref=badge_shield)


[Bencode](https://en.wikipedia.org/wiki/Bencode) is the encoding used by the peer-to-peer file sharing system
[BitTorrent](https://opensource.org/licenses/MIT) for storing and transmitting loosely structured data.

This is a pure PHP library that allows you to encode and decode Bencode data.

This library is fork from [OPSnet/bencode-torrent] / [Rhilip/Bencode] (https://github.com/OPSnet/bencode-torrent),
with same method like [sandfoxme/bencode](https://github.com/sandfoxme/bencode)

## Installation

```shell script
composer require theonedt/bencode
```

## Usage

```php
<?php

require '/path/to/vendor/autoload.php';

use Rhilip\Bencode\Bencode;
use Rhilip\Bencode\ParseErrorException;

// Decodes a BEncoded string
Bencode::decode(string $string);

// Encodes string/array/int to a BEncoded string
Bencode::encode(mixed $data);

// Decodes a BEncoded file From path
Bencode::load(string $path); 

// Encodes string/array/int to a BEncoded file
Bencode::dump(string $path, mixed $data); 

// With Error Catch
try {
    Bencode::decode('wrong_string');
 } catch (ParseErrorException $e) {
    // do something
} 
```

## License

The library is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FRhilip%2FBencode.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2FRhilip%2FBencode?ref=badge_large)