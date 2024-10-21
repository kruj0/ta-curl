# TA-CURL

## Overview

TA-CURL is a Splunk add-on that provides a user-friendly way to make HTTP requests using Curl. 
This app is a fork of TA-Webtools and includes modifications to allow configuration of the `verify` parameter and the use of self-signed certificates.

## Features

- Support for HTTP methods: GET, POST, PUT, DELETE, PATCH, and HEAD
- Authentication support via Splunk session keys, usernames and passwords, and tokens
- Configuration for the use of self-signed certificates or with a verify=false
- Configuration for the use of client certificates
- Flexible error handling and logging
- Support for custom headers

## License

TA-CURL is licensed under the Apache 2.0 License. The entire codebase is derived from TA-Webtools, with modifications made to support the features listed above.

## Installation

1. Clone the repository or download the ZIP file.
2. Unzip the file and move the `ta-curl` folder to the `Splunk/etc/apps/` directory.
3. Restart Splunk.

## Usage

You can use the add-on by executing `curl` commands in your Splunk search. For more information on syntax and available options, please refer to the official documentation or the examples in the code.
### Command Syntax

Here is an example of how to use the TA-CURL add-on in Splunk:
```
| curl 
method="GET" 
verify=true/false/Path_to_selfsigned_cert.pem
url="https://api.example.com/data" 
```