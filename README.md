# pcaps

The arista-sll-interface-any.pcap file contains a pcap of the router control plane traffic on veos.  it was captured using the
-i any parameter to tcpdump, which causes each packet to be encapsualted in an SLL header (see https://github.com/the-tcpdump-group/libpcap/blob/master/pcap/sll.h)

Bytes 14 and 15 of this SLL header contain either an ethertype, a value from 1-4 or some other arbitrary numbers.  type 4 indicates
and LLC header.
