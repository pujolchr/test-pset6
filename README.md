# Test suite for Cs50 pset6 server.c #

https://cdn.cs50.net/2014/fall/psets/6/pset6/pset6.html

Before working on Pset6 of Cs50 I wanted to  implement an "test suite" which compare
the cs50 staff solution output to mine.

Principle is to use `diff` between the outputs of the same `telnet`
request passed to the staff implementation and mine.  

The `test-pset6` scrpit read a text file containing requests for the server,
use `telnet` to send the request to both server,
and check the two answer for difference with `diff`.  
If there is any diffeence for a particular request
the test is considered faile for this request.

### How to install in the cs50 appliance.
* using  Git:
  `$ git clone https://github.com/pujolchr/test-pset6`

* using wget:
  `$ wget https://github.com/pujolchr/test-pset6/archive/master.zip`  
  `$ unzip master.zip`

### How to run the test.

usage:  
    `test-pset6 host port port [FILE]`

the test supose that the two implementations run on the same IP adress 
serving the same file but with different port.

* Run the staff implementation
  Note the port number.
* Run your implementation to serve the same file than the the staff implementation  
  Note the the port number used by your implementation.  
* run the test file:  
  Usage: `test-pset6 host port port [FILE]`  
  whith :  
  * host: IP adress of the two server
  * port: port numbers of the two server
  * [FILE]: file containing the request to pass to the servers
    if no file name is provided `test-pset6` will try to used the file
    `test.txt` in the same directory than `test-pset6`

### Structure of the "test file"
The file used by `test-pset6` is a simple text file containing request.
One request per line.

