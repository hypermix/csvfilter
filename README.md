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

If you want to read character by utf8 from csv made by cp949, do shown as below.
```
stream_filter_register('convert.transcode.cp949', 'CsvFilter\FilterTranscode');
...
$reader->appendStreamFilter('convert.transcode.cp949');
```

# License
The MIT License (MIT)
Copyright (c) 2016 hypermix

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
