# TCPDUMP_Commands
Examples of TCPDUMP filters

When working on an organizational network there are times whem the only tool we have available to monitor the netwrok activity of a device is TCPDUMP. We have seen many systems with a Linux kernel have an installation of TCPDUMP on them for troubleshooting purposes. Having TCPDUMP allows the troubleshooting team to find out if there is any anomolous traffic traversing the system. It is important to know how to use TCPDUMP in order to perform network monitoring with only a command-line console available.

There are certain macros utilized in the capturing of traffic using TCPDUMP. These include:
- host
- net
- port
- src host
- dst host
- src net
- dst net
- src port
- dst port
- icmp
- tcp
- udp

For example, if we only wanted to capture network traffic from source host 172.16.1.27, we could us the 'src host' macro.
<pre><code>sudo tcpdump -nnvvvv -i ens33 src host 172.16.1.27</code></pre>

If we only wanted to capture network traffic from source network 172.16.1.0/24, we could us the 'src net' macro.
<pre><code>sudo tcpdump -nnvvvv -i ens33 src net 172.16.1.0/24</code></pre>
