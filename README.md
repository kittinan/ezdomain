## About EZDomain
EZdomain is based on python programming tool that use to enumerate and manipulate the domains such as subdomains, directory, S3 bucket by customizing the position of the payload in the URL.

## Installation
```
git clone https://github.com/mayaseven/ezdomain.git
```

## Dependencies
Python modules (requests, argparse, tqdm, multiprocessing, termcolor)

- Installation on Windows:
```
c:\python27\python.exe -m pip install -r requirements.txt
```

- Installation on Linux and MacOSX
```
sudo pip install -r requirements.txt
```

## Usage

| Short        | Long       | Description
| ------------ |------------|------------
| -d           | --domain   | Providing a domain name (ex. domain-*.com)
| -w           | --wordlist | Providing a path of a wordlist file
| -o           | --output   | Providing a path of output file
| -t           | --thread   | Providing a thread number (default is 3)
| -x           | --exclude  | Providing a exclude output status code (ex. -x 443,404)
| -h           | --help     | show this help message and exit

### Examples
* To list all the options use -h\
```python ezdomain.py -h```

* To find the sub-domains\
```python ezdomain.py -d "http://*.domain.com/" -w words/subdomains-10000.txt -o domain.out -x 404```

* To find the directory in the domain (You can exclude the 403 status code to find only a public bucket)\
```python ezdomain.py -d "https://domain.com/*" -w words/directory.txt -o domain.out```

* To find the S3 bucket (You can exclude the 403 status code to find only a public bucket)\
```python ezdomain.py -d "http://company-*.s3.amazonaws.com/" -w words/name.txt -o s3.out -x 404```

## License
License of ezdomain is under GNU GPL license. [LICENSE](https://github.com/MAYASEVEN/ezdomain/blob/master/LICENSE)

### Version
**Current version is 1.0**
