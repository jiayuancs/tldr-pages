# tcpdump [modified]

> Dump traffic on a network.
> More information: <https://www.tcpdump.org>.

- 列出所有可用的网卡：

`tcpdump -D`

- 指定要捕获的网卡，默认捕获第一个网卡的数据，使用 any 表示捕获所有网卡数据：

`tcpdump -i {{eth0}}`

- 将捕获的数据保存到文件中，该文件可被 wireshark 打开：

`tcpdump -w {{dumpfile.pcap}}`

- 读取 .pcap 文件：

`tcpdump -r {{dumpfile.pcap}}`

- Capture all TCP traffic showing contents (ASCII) in console:

`tcpdump -A tcp`

- Capture the traffic from or to a host:

`tcpdump host {{www.example.com}}`

- Capture the traffic from a specific interface, source, destination and destination port:

`tcpdump -i {{eth0}} src {{192.168.1.1}} and dst {{192.168.1.2}} and dst port {{80}}`

- Capture the traffic of a network:

`tcpdump net {{192.168.1.0/24}}`

