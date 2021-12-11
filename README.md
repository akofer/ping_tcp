# ping_tcp

The best tool to detect delay and bandwith of a tcp connection between two computers (other than ping without bandwith info).

Usage:

Before we start detection, the tcp server program named ping_tcp_srv should be run on the remote computer as below:

$ ./ping_tcp_srv 8080    # start on port 8080

And then run the tcp client program named ping_tcp on the local computer (here we assume its ip is 192.168.1.100),

./ping_tcp 192.168.1.100 8080    # ping the tcp server with ip 192.168.100.1 and port 8080

And then just check the outputs on the local computer. They look like below:

$ ./conn_ping.py 192.168.1.100 8080
225280 bytes sent/recv via 192.168.1.100 tcp port 8080: seq=0 time=1020.114 ms speed=215.662KB/s
307200 bytes sent/recv via 192.168.1.100 tcp port 8080: seq=1 time=1186.439 ms speed=252.858KB/s
368640 bytes sent/recv via 192.168.1.100 tcp port 8080: seq=2 time=1004.536 ms speed=358.374KB/s
491520 bytes sent/recv via 192.168.1.100 tcp port 8080: seq=3 time=1008.034 ms speed=476.174KB/s
327680 bytes sent/recv via 192.168.1.100 tcp port 8080: seq=4 time=1142.953 ms speed=279.977KB/s
768000 bytes sent/recv via 192.168.1.100 tcp port 8080: seq=5 time=1009.583 ms speed=742.881KB/s
409600 bytes sent/recv via 192.168.1.100 tcp port 8080: seq=6 time=1005.742 ms speed=397.716KB/s
327680 bytes sent/recv via 192.168.1.100 tcp port 8080: seq=7 time=1661.284 ms speed=192.622KB/s

ping_tcp will run for ever and can be stopped by ctrl-c.
