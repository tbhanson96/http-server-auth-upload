# Disclaimer

This is a fork from : https://github.com/indexzero/http-server/ (thank you to all collaborators on the project)  

Forked in order to add Basic Auth in it.    
This repo will mostly be deleted when the original project will add Auth.  

# http-server-with-auth: a command-line http server

`http-server-with-auth` is a simple, zero-configuration command-line http server.  It is powerful enough for production usage, but it's simple and hackable enough to be used for testing, local development, and learning.

# Installing globally:

Installation via `npm`:

     npm install http-server-with-auth -g

This will install `http-server` globally so that it may be run from the command line.

## Usage:

     http-server-with-auth [path] [options]

`[path]` defaults to `./public` if the folder exists, and `./` otherwise.

# Installing as a node app

     mkdir myapp
     cd myapp/
     jitsu install http-server-with-auth

*If you do not have `jitsu` installed you can install it via `npm install jitsu -g`*

## Usage

### Starting http-server locally

     node bin/http-server-with-auth

*Now you can visit http://localhost:8080 to view your server*

## Available Options:

`-p` Port to use (defaults to 8080)
 
`--username` Username for basic authentication [none]

`--password` Password for basic authentication [none]

`-a` Address to use (defaults to 0.0.0.0)

`-d` Show directory listings (defaults to 'True')

`-i` Display autoIndex (defaults to 'True')

`-g` or `--gzip` When enabled (defaults to 'False') it will serve `./public/some-file.js.gz` in place of `./public/some-file.js` when a gzipped version of the file exists and the request accepts gzip encoding.

`-e` or `--ext` Default file extension if none supplied (defaults to 'html')

`-s` or `--silent` Suppress log messages from output

`--cors` Enable CORS via the `Access-Control-Allow-Origin` header

`-o` Open browser window after starting the server

`-c` Set cache time (in seconds) for cache-control max-age header, e.g. -c10 for 10 seconds (defaults to '3600'). To disable caching, use -c-1.

`-U` or `--utc` Use UTC time format in log messages.

`-P` or `--proxy` Proxies all requests which can't be resolved locally to the given url. e.g.: -P http://someurl.com

`-S` or `--ssl` Enable https.

`-C` or `--cert` Path to ssl cert file (default: cert.pem).

`-K` or `--key` Path to ssl key file (default: key.pem).

`-r` or `--robots` Provide a /robots.txt (whose content defaults to 'User-agent: *\nDisallow: /')

`-h` or `--help` Print this list and exit.
