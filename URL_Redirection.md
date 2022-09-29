**Title**
Redirection to possible attacker page

**Type of vulnerability**
URL Redirection

**Endpoint**
https://hackxpert.com/ratsite/GoToPage.php

**Description**
Thanks to page opener section an attacker could create a link https://hackxpert.com/ratsite/GoToPage.php?url=https%3A%2F%2Ftwitter.com%2Ffrancisco_melov
and use the page and redirect to a malicious page, the atacker could crate a clone page and steal the user info

**Steps to reproduce**
*Steps*
1. The attacker could send a url https://hackxpert.com/ratsite/GoToPage.php?url=https%3A%2F%2Ftwitter.com%2Ffrancisco_melov
2. if the victim opens the url he will be sent to the attackers page withput knowing it


**Impact**
The attacker could send the victim wherever he wants, to a clone page and steal everything he types thinking he is in the real page

