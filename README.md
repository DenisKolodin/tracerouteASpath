tracerouteASpath
================

Builds an AS Path table for an input file of IP addresses
Written in Golang, it runs traceroutes concurrently and parses out the IP address.
The list of IPs is used to query the PTR record and origin ASN of the IP address.

This program requires many open files (ulimit -n 4096), because of the number of instances of traceroute being run.

TODO:
* Add File output for both Traceroute hops and AS path (+ Prefix)
* Parse file to find corrupt/missing results
* * Re-run traceroute on these results
* Add probe to determine maximum number of concurrent traceroutes that should be run
* IPv6 Support
