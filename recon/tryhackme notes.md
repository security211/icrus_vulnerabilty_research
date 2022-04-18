-   `whois`
-   `dig`, `nslookup`, `host`
-   `traceroute`/`tracert`

## dig
Domain Information Groper -provides alot of info about domains

** dig @1.1.1.1 tryhackme.com

## host
shows how many host are in a given ip

## whois
gives ifo about the blog

## special search engines

### ViewDNS.info

[VidewDNS.info](https://viewdns.info/) offers _Reverse IP Lookup_. Initially,

### Threat Intelligence Platform

[Threat Intelligence Platform](https://threatintelligenceplatform.com/) requires you to provide a domain name or an IP address, and it will launch a series of tests from malware checks to WHOIS and DNS queries. The WHOIS and DNS results are similar to the results we would get using `whois` and `dig`, but Threat Intelligence Platform presents them in a more readable and visually appealing way.

#### Censys

[Censys Search](https://search.censys.io) can provide a lot of information about IP addresses and domains. In this example, we look up one of the IP addresses that `cafe.thmredteam.com` resolves to. We can easily infer that the IP address we looked up belongs to Cloudflare. We can see information related to ports 80 and 443, among others;

#### Shodan

You might remember using [Shodan](https://www.shodan.io/) in the [Passive Reconnaissance](https://tryhackme.com/room/passiverecon) room. In this section, we will demonstrate how to use Shodan from the command line.
