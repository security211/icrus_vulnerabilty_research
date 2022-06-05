Why Haktrails
Building a huge distributed recon system is great and all but at some point it becomes more cost/time effective to just pay for access to recon data that someone else has gathered. Working with APIs can be a bit awkward though. Wouldn’t it be lovely if there was a nifty little tool that did all of the API calls for you, and integrated nicely with your existing tools? 🤔

Yes. Yes it would! That’s exactly what haktrails does.

Features
Stdin input for easy tool chaining
“JSON” or “list” output options for easy tool chaining
Subdomain discovery
Associated root domain discovery
Associated IP discovery
Historical DNS data
Historical whois data
Company discovery (discover the owner of a domain)
Whois (returns json whois data for a given domain)
Ping (check that your current SecurityTrails configuration/key is working)
Usage (check your current SecurityTrails usage)
How to Use It
Setting Up the Config File
Before you do anything, you need to create a config file. The default location for the config file is:

~/.config/haktools/haktrails-config.yml 
The config file should look like this:

securitytrails:
  key: <your api key>
You are all hackers so I know I don’t need to say this, but make sure you replace “<your api key>” with your actual SecurityTrails API key.

Installing the Tool
First, install golang on your computer, then run the following command:

go get github.com/hakluke/haktrails
You should now have the haktrails binary at ~/go/bin/haktrails. If you haven’t already, I’d recommend adding ~/go/bin/ to your $PATH so that you can just type haktrails instead of ~/go/bin/haktrails.

Using the Tool
Note
Note: In these examples, domains.txt is a list of root domains that you wish to gather data on. For example:

hakluke.com
bugcrowd.com
tesla.com
yahoo.com
Flags
The output type can be specified with -o json or -o list. List is the default. List is only compatiable with subdomains, associated domains and associated ips. All the other endpoints will return json regardless.
The number of threads can be set using -t <number>. This will determine how many domains can be processed at the same time. It’s worth noting that the API has rate-limiting, so setting a really high thread count here will actually slow you down.
The config file location can be set with -c <file path>. The default location is ~/.config/haktools/haktrails-config.yml. A sample config file can be seen below.
The lookup type for historical DNS lookups can be set with -type <type>, available options are a,aaaa,mx,txt,ns,soa.
Warning
Warning: With this tool, it’s very easy to burn through a lot of API credits. For example, if you have 10,000 domains in domains.txt, running cat domains.txt | haktrails subdomains will use 10,000 credits. It’s also worth noting that some functions (such as associated domains) will use multiple API requests, for example, echo "yahoo.com" | haktrails associateddomains would use about 20 API requests, because the data is paginated and yahoo.com has a lot of associated domains.

Gathering subdomains
This will gather all subdomains of all the domains listed within domains.txt.

cat domains.txt | haktrails subdomains
Of course, a single domain can also be specified like this:

echo "yahoo.com" | haktrails subdomains
Gathering associated domains
“Associated domains” is a loose term, but it is generally just domains that are owned by the same company. This will gather all associated domains for every domain in domains.txt

cat domains.txt | haktrails associateddomains
Gathering associated IPs
Again, associated IPs is a loose term, but it generally refers to IP addresses that are owned by the same organisation.

cat domains.txt | haktrails associatedips
Getting historical DNS data
Returns historical DNS data for a domain.

cat domains.txt | haktrails historicaldns
Getting historical whois data
Returns historical whois data for a domain.

cat domains.txt | haktrails historicalwhois
Getting company details
Returns the company that is associated with the provided domain(s).

cat domains.txt | haktrails company
Getting domain details
Returns all details of a domain including DNS records, alexa ranking and last seen time.

cat domains.txt | haktrails details
Getting whois data
Returns whois data in JSON format.

cat domains.txt | haktrails whois
Getting domain tags
Returns “tags” of a specific domain.

cat domains.txt | haktrails tags
Getting API Usage Data
Returns data about API usage on your SecurityTrails account.

haktrails usage