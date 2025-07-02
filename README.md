# httpflood

Sending simultaneous and continuous traffic to a webserver or a web application

* On Linux, run `ulimit -n 999999` beforehand.
* Safely create over 1000 simultaneous connections by using golang goroutine.
* 100~300 connections can down a normal website in 10 seconds, specially apache server.
* Selectable GET or POST
* Can generate random URL
* Accept custom header 

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
    ```
    $ go build
    ```
5. Create custom `header.txt` file <br>
    ```
    Accept: text/html
    User-agent: Wget
    Referer: http://google.com
    ```
6. Run the application
    ```
    $ ./httpflood  <url> <threads> <get/post> <seconds> <header.txt/nil>
    ```


