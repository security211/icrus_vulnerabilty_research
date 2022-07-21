Brute Force 
brute force subdomains with sublister,knockpy
github

learn jq

curl -k -s [https://sonar.omnisint.io/subdomains/tesla.com](https://sonar.omnisint.io/subdomains/tesla.com) | jq -r ‘.[]’ | sort -u

https://github.com/Cgboal/SonarSearch
sonar search api
for searching this things

curl -k -s “https://crt.sh/?q=tesla.com&output=json" | jq -r ‘.[] | “\(.name_value)\n\(.common_name)”’ | sort -u

cert.sh use it to learn about certificates


while running sublister use the -v option to get more from the input

