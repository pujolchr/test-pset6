# Test suite for Cs50 pset6 server.c #

https://cdn.cs50.net/2014/fall/psets/6/pset6/pset6.html

Before working on Pset6 of Cs50 i implement an "test suite" which compare
the cs50 staff solution output to mine.

Principle is to use diff between the output of the same telnet
request passed to the staff implementation and mine.

usage: test-pset6 host port port [FILE]

the test supose that the two implementations run on the same IP adress 
serving the same file but with different port.


