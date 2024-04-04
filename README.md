# Subdomain Enumeration Script using crt.sh API

This Python script performs subdomain enumeration using the crt.sh API. It can fetch subdomains for a target domain specified either directly or from a file containing a list of domain names. The script supports recursive search for subdomains and can include wildcard subdomains in the output.

## Requirements

- **Python 3**: The programming language used to write this script.
- **argparse**: A Python module used for command-line argument parsing.
- **requests**: A Python library used for making HTTP requests.
- **json**: A Python module used for handling JSON data.

## Installation

### 1. Install Python 3

If you don't have Python 3 installed on your system, you can download and install it from the [official Python website](https://www.python.org/downloads/).

### 2. Install required Python packages

You can install the required Python packages using pip, the package installer for Python. Open your terminal and run the following commands:

```bash
pip install requests
```

## Usage

```bash
python3 script.py [Options]
```

### Options

- `-d, --domain`: Specify the target domain to get subdomains from crt.sh.
- `-f, --file`: File containing domain names, one per line.
- `-r, --recursive`: Perform a recursive search for subdomains.
- `-w, --wildcard`: Include wildcard subdomains in the output.
- `-o, --output`: Output file path to save the results.

### Examples

1. To fetch subdomains for a specific domain:
```bash
python3 script.py -d google.com
```

2. To fetch subdomains from a file:
```bash
python3 script.py -f domains.txt
```
- `domains.txt` should contain a list of domain names, one per line.

3. To perform a recursive search and include wildcard subdomains:
```bash
python3 script.py -d example.com -r -w
```

## Output

The script will print the discovered subdomains to the standard output or save them to a specified output file. If the recursive option is enabled, it will continue searching for subdomains recursively and print or save the results accordingly.

## Error Handling

The script has basic error handling to manage exceptions that may occur during the HTTP requests or JSON parsing.

## Notes

- The script uses the crt.sh API to fetch subdomains. It may be subject to rate limiting or other restrictions imposed by the API.
- The script does not verify the existence or validity of the discovered subdomains; it simply retrieves them from the crt.sh database.

**Note:** Make sure to replace `script.py` and `domains.txt` with the actual script filename and domain list filename, respectively.
