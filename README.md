# Information

South Park Downloader to get South Park episodes from official sources.

# Features

 - Cross-platform support.
 - Full support for English and German episodes.
 - Ready for additional languages.
 - Renaming of episodes to contain the title of each language.
 - Checksum verification of downloaded files.
 - Fix audio delay for certain acts.

# Requirements

 - PHP (>= 5.5.9) from http://php.net/downloads.php
 - FFmpeg from http://ffmpeg.zeranoe.com/builds/
 - mkvmerge (>= 9.7, part of MKVToolnix) from http://www.bunkus.org/videotools/mkvtoolnix/downloads.html

Or, if you are using Windows, just take the bundle of pre-packaged tools from https://github.com/craue/SouthParkDownloader/releases. 

# Installation

Run the following commands in a shell to set up the required dependencies:

```sh
php -r "eval('?>'.file_get_contents('http://getcomposer.org/installer'));" -- --install-dir=vendor
php vendor/composer.phar install
```

# Configuration

 - Copy one of the `config-sample-*.php` files to `config.php`.
 - Edit `config.php` and set all the values to fit your environment.

# Usage

To download all episodes of season 15 in English:

	php download.php s=15 l=en

To download episode 8 of season 13 in German and English, while taking video from the German source and setting the default audio language to German:

	php download.php s=13 e=8 l=de+en
