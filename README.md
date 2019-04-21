## Slowloris
A Node.js implementation of the slowloris attack. With TLS Support.

## What is Slowloris?
> Slowloris is DDoS attack software that enables a single computer to take down a web server. Due the simple yet elegant nature of this attack, it requires minimal bandwidth to implement and affects the target server’s web server only, with almost no side effects on other services and ports.
Slowloris works by opening multiple connections to the targeted web server and keeping them open as long as possible. It does this by continuously sending partial HTTP requests, none of which are ever completed. The attacked servers open more and connections open, waiting for each of the attack requests to be completed.
Periodically, the Slowloris sends subsequent HTTP headers for each request, but never actually completes the request. Ultimately, the targeted server’s maximum concurrent connection pool is filled, and additional (legitimate) connection attempts are denied.
[source](https://www.imperva.com/learn/application-security/slowloris/)

## Installation
```
npm install -g slowloris-attack
```
## Usage
```
slowattack [options] <url>

Options:
  -V, --version      output the version number
  -p, --port <n>     The port of the webserver (default: 80)
  -s, --sockets <n>  Number of sockets to use (default: 200)
  -t, --time <n>     Duration of the attack in milliseconds
  -h, --help         output usage information
  ```

Note that this utility is intended for testing purposes.
## License 
[MIT License]https://opensource.org/licenses/MIT
