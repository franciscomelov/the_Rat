Bug report template in markdown:


**Title**
Hidden endpoint exposes client details to all users

**Type of vulnerability**
Broken Access Control

**Endpoint**
https://UncleRatsCheeseShop.com/api/v1/getClients

**Description**
Users can only view the details of their own clients as intended, however when they make a GET call to /api/v1/getClients, the user can view all the clients in the system.
This endpoint is normally not available in the UI but we can trigger a call to /api/v2/getClients by clicking the by clicking the "View clients" button.
The call to this endpoint shows the users own clients as intended.

**Steps to reproduce**
*Requirements*
1. MiTM proxy such as burp
2. User with "Salesmen" priviledges
	2a. Salesman privlidges can only view their own clients

*Steps*
1. Login to the application
2. Navigate to clients module
	2a. Make sure you have the MiTM proxy enabled
3. Click the "View clients" button
4. In the MiTM proxy, click the "history" tab and find the call to /api/v2/getClients
5. Send the request to the repeater and replace the V2 with V1 
	5a. /api/v2/getClients >>> /api/v1/getClients
6. Resend the request

**Impact**
attacker can view all the clients, even those that do not belong to him

**Remidiation**
Disable the old API endpoint

**Severity**
High

