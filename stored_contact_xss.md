**Title**
sotred xss in table contacts table

**Type of vulnerability**
stored xss

**Endpoint**
https://hackxpert.com/ratsite/newContact.php

**Description**
An attacker is able to create a new contact but if in the email input he writes "<iframe src=javascript:prompt()>, an  xss qil be stored in the contact list, if later someone search for said contect the xss will pop up malicious code

**Steps to reproduce**

*Steps*
1. go to https://hackxpert.com/ratsite/newContact.php
2. input and name and an email 
3. in the email input write "<iframe src=javascript:prompt()>
4. Now if someone looks for that user the xss will be executed


**Impact**
an attacker could create a contact and share executing code in ecery user that sees it , since is an stored xss it will be saved in the server


