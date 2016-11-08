# CsvFilter

CSV Transcode Filter For League/Csv
Transcode file also belongs to League/Csv's repository.
This Repository will be useful for Composer beginners.

# How To Use
1. Installation
2. Usage

## 1. Installation

### Composer
```
"hypermix/csvfilter": "dev-master"
```

## 2. Usage

```
use League\Csv\Reader;
use CsvFilter\FilterTranscode;
```

```
stream_filter_register('convert.transcode.XXX', 'CsvFilter\FilterTranscode');
$reader = Reader::createFromPath('input.csv');
$reader->appendStreamFilter('convert.transcode.XXX');
```
XXX is Enconding of file.

if you want to read character by utf8 from csv made by cp949, do it like below code.
```
stream_filter_register('convert.transcode.cp949', 'CsvFilter\FilterTranscode');
...
$reader->appendStreamFilter('convert.transcode.cp949');
```

