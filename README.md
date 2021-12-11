# Ping via TCP Connections

To detect **both delay and bandwith** between two computers via a tcp connection, this project aims to provide simply the best solution.

# Usage

First run `ping_tcp_srv` on the remote computer as below. It will starts a tcp server.
```
$ ./ping_tcp_srv 8080    # start on port 8080, and we assumed its ip as 192.168.100.1
```
Then run `ping_tcp` on the local computer. It will stars a tcp client to do detections and output realtime results to stdout.
```
$ ./ping_tcp 192.168.1.100 8080    # ping the tcp server with ip 192.168.100.1 and port 8080
225280 bytes sent/recv via 192.168.1.100 tcp port 8080: seq=0 time=1020.114 ms speed=215.662KB/s
307200 bytes sent/recv via 192.168.1.100 tcp port 8080: seq=1 time=1186.439 ms speed=252.858KB/s
368640 bytes sent/recv via 192.168.1.100 tcp port 8080: seq=2 time=1004.536 ms speed=358.374KB/s
491520 bytes sent/recv via 192.168.1.100 tcp port 8080: seq=3 time=1008.034 ms speed=476.174KB/s
327680 bytes sent/recv via 192.168.1.100 tcp port 8080: seq=4 time=1142.953 ms speed=279.977KB/s
768000 bytes sent/recv via 192.168.1.100 tcp port 8080: seq=5 time=1009.583 ms speed=742.881KB/s
409600 bytes sent/recv via 192.168.1.100 tcp port 8080: seq=6 time=1005.742 ms speed=397.716KB/s
327680 bytes sent/recv via 192.168.1.100 tcp port 8080: seq=7 time=1661.284 ms speed=192.622KB/s
```
`ping_tcp` will run for ever and can be stopped by `ctrl-c`.

# Implementations

There are several implementations using different program languages, including Python, C, Go, etc.. We promise they work the same except performance limitations of languages. Choose any one as you wish. 
