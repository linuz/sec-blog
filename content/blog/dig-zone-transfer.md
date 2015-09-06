Title: Initiate zone transfer using Dig
Date: 2015-09-05 21:24
Tags: Commands, Red Team

[Dig](http://linux.die.net/man/1/dig) is a DNS lookup utility. You can use Dig to initiate a [DNS zone transfer](https://en.wikipedia.org/wiki/DNS_zone_transfer) from a DNS server that allows it. This is useful to for finding sensitive information such as hostnames.

`dig @<dnsserver> <domain> axfr`

For example:

`dig @dns.example.org example.org axfr` 
