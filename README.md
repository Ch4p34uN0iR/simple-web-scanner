# Simple web scanner

## Installation

This program uses `python 3`. I recommend you use linux in virtualenv.
You can test your python enviroment by the following commands:

```
$ /usr/bin/python3 --version
Python 3.5.2
```

### Requirements packages:

You can install the following packages:
```
pip install bs4
```



## Usage:

- If you don't know how to use it. Type the following command:
```
./scan_cli.py -h
```

- So, You have to define `seed_url` and `engine` arguments for this program.

```
python3 scan_cli.py --seedurl http://203.249.90.9:5000 --engine xss
```


## Program structure

```
.
├── crawler.py      # Simple webcrawler
├── parser.py       # HTML parser
├── README.md       # You are here
├── scan_cli.py     # main program, but it is not important.
├── scanner_core.py # core scanner. Read this script carefully
├── sqli_scanner.py # SQL injection which extented from core scanner
├── vectors         # attacker vectors directory
│   ├── sqli_vectors.txt
│   └── xss_vectors.txt
└── xss_scanner.py  # XSS which extented from core scanner
```

- If you want to know how crawler works. First, you have to modify `seed_url` line 89 in file crawler, then you can run `python3 crawler.py` to run crawler.
