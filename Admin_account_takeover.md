Bug report template in markdown:


**Title**
users are able to get admin account, 

**Type of vulnerability**
Admin account takeover

**Endpoint**
https://hackxpert.com/ratsite/userSettings.php

**Description**
In the account setting a user could get admin privileges by changing parameters in the inputs
and an admin panel is shoen, whe the attacker is able to modify others users permissions 

**Steps to reproduce**
*Steps*
1. go to account setting https://hackxpert.com/ratsite/userSettings.php
2. inspect the submit button
3. in the devtools, above the submit button you can see the next  hidden input
4. input type="text" value="0" id="isAdmin" name="isAdmin" hidden=""
5. chage value="0" to value="1"
6. click in the submit button and now you have an admin account
7. now you have acces to an admin panel https://hackxpert.com/ratsite/users.php? where you can modify other users privileges

**Impact**
By gettin admin privileges an attacker is able to access an admin panel  https://hackxpert.com/ratsite/users.php? 
here, the attacker is able to modify other user privileges and grant admin privileges to anoter user or delete admin privileges to legit admins

