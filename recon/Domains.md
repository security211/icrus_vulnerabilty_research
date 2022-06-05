run whois look up using lookup.icann.org

ViewDNS.info gives you info about your sudomain


## Active Recothis is gaing info by interacting wi=with the information system



## Passive Recon
In passive reconnaissance, you rely on publicly available knowledge

whois query the whois servers
nslookup to query DNS servers
dig to query DNS servers

whois
dnsdumpster 
shodan.io
nslookup thmlabs.com

Dig  & nslookup are used to check dns for ip adresses used.

dns dumpster digs out dns information and shares it with the user


reverse dns
use domain creators emails to search for what they have also registerd
[viewdns.info](http://viewdns.info/reversewhois/)




One can us e censys to search for domanis

https://censys.io/certificates?q=.example.com

Before You must need to install censys (See For installation guide)in your machine using pip

$pip install censys
# Configure your credentials
$ censys config
#Now we have successfully Install censys cli to check just type censys

censys search 'services.http.response.html_title: "Facebook
"' --index-type hosts | jq -c '.[] | {ip: .ip}’

Command: censys search ' services.tls.certificates.leaf_data.subject.common_name: "facebook.com"' --index-type hosts | jq -c '.[] | {ip: .ip}' > ip.txt

#we will use sed command to delete some char from our ip.txt file

Command: sed -i 's/[^0-9,.]*//g' ip.txt