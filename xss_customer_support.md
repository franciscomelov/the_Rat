**Title**
An attacker could send a link to use another user to send malicious code

**Type of vulnerability**
deflected xss

**Endpoint**
https://hackxpert.com/ratsite/angular_test.php

**Description**
an atacker coul share a link with a xss payload if another user uses it, malicious code will be sent from the victims account

**Steps to reproduce**
*Steps*
1. An attacker shares this link https://hackxpert.com/ratsite/angular_test.php?q={{%27a%27.constructor.prototype.charAt=[].join;$eval(%27x=1}%20}%20};alert(1)//%27);}}
2. if a victim clicks it malicious code will be sent to customer support from their account

or if the attacker want to send te xss themself he could write this payload in the message input and send it {{'a'.constructor.prototype.charAt=[].join;$eval('x=1} } };alert(1)//');}}

**Impact**
an atacker could use other users to share malicious code, and the victims  could be considered attackers since the code will be sent from their accounts



