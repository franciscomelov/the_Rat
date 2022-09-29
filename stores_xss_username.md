Bug report template in markdown:


**Title**
stored xss in user name

**Type of vulnerability**
sotores xss

**Endpoint**
https://hackxpert.com/ratsite/login.php

**Description**
An attacker could usean xss payload in the username to stored xss attack

**Steps to reproduce**
*Steps*
1.go to the login page https://hackxpert.com/ratsite/login.php
2. inthe name saction write this payload "><img src=x onerror=prompt()>
3. the payload will be saved and every time someone sees the username a pop up will appear


**Impact**
by sharing the user with the xss payload other user could get malicious code executed in ther browsers
