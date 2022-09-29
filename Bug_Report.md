**Title**
deflected xss attack

**Type of vulnerability**
dom and 

**Endpoint**
https://hackxpert.com/ratsite/contacts.php

**Description**
By using this pyload in the text input you could pop up a prompt
By sending this url to another user you could make use oa xss vulnerability
hackxpert.com/ratsite/contacts.php?searchTerm="<iframe src=javascript:prompt()>
"<iframe src=javascript:prompt()>

**Steps to reproduce**

*Steps*
Dom based xss
1. go to https://hackxpert.com/ratsite/contacts.php
2. paste this code in the search input "<iframe src=javascript:prompt()>
3. click search, and you will get a pop up

deflcted based xss
1. By sending this url to another user
	hackxpert.com/ratsite/contacts.php?searchTerm="<iframe src=javascript:prompt()>
to anothet user you clud inject code in their  web browser


**Impact**
Xss attacks could inject malicious code in the browser


