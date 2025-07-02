# httpflood

Sending simultaneous and continuous traffic to a webserver or a web application

* On Linux, run `ulimit -n 999999` beforehand.
* Safely create over 1000 simultaneous connections by using golang goroutine.
* 100~300 connections can down a normal website in 10 seconds, specially apache server.

**Why can it run over 1000 threads(goroutines)? [Read this](http://tleyden.github.io/blog/2014/10/30/goroutines-vs-threads/)**

 - HTTP GET
 - HTTP POST
 - Random url
 - Custom header

 Default header setting:
 - Random user-agents
 - Random AcceptAll
 - Random Referer for GET
 - Random data for POST 


# Usage

1. Download and install golang
2. Clone the repository <br>
    ```
    $ git clone https://github.com/tantowi/httpflood httpflood
    $ cd httpflood
    ```
3. Compile the application <br>
    `$ go build`
4. Create custom `header.txt` file <br>
    ```
    Accept: text/html
    User-agent: Wget
    Referer: http://google.com
    ```
5. Run the application
    `./httpflood  <url> <threads> <get/post> <seconds> <header.txt/nil>`


