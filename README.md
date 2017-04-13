# Simple web scanner

This is simple web application fuzzer for scanning SQL injection and XSS vulnerabilities on the Internet. It is helpful for understanding how to detect SQL injection and XSS by automatic tool.

## User guide

This program uses python 3. I recommend using virtualenv for testing purpose. To check our python enviroment, you can use the following commands:

```
$ python3 --version
Python 3.5.2

$ pip3 --version
pip 9.0.1 from /usr/local/lib/python3.5/dist-packages (python 3.5)
```

### Requirements packages:

BeautifulSoup are used for parsing HTML content. You can install it by command:
```
pip3 install bs4
```



## Usage:

So, you have to define `seed_url` and `engine` arguments for this program.

```
python3 scan_cli.py --seedurl http://example.com --engine xss
```


## Program structure

```
.
├── crawler.py      # Simple webcrawler
├── parser.py       # HTML parser
├── README.md       # You are here
├── scan_cli.py     # main program, but it is not important. It just parses command line arguments
├── scanner_core.py # core scanner. Read this script carefully
├── sqli_scanner.py # SQL injection which extented from core scanner
├── vectors         # attacker vectors directory
│   ├── sqli_vectors.txt
│   └── xss_vectors.txt
└── xss_scanner.py  # XSS which extented from core scanner
```

## Notes

If you want to know how crawler works. You have to modify `seed_url` line 89 in file crawler, then you can run `python3 crawler.py` to see what happened.
