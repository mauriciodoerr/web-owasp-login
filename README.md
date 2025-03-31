# web-owasp-login

Post-graduate exercisse:

> As per OWASP ASVS, what are the recommendations on password usage. What is the CWE and descibre its best practices.
> 
> As a challenge, create a login screen with user and password following OWASP and CWE recommendations.


## OWASP
Based on latest stable release: [OWASP ASVS 4.0.3](https://github.com/OWASP/ASVS/tree/v4.0.3/4.0), following CWEs are part of OWASP _v2.1 Password Security_:
1. CWE-521: Weak Password Requirements
2. CWE-620: Unverified Password Change
3. CWE-263: Password Aging with Long Expiration

As best-practices to mitigate above CWEs, implement as follows:
* Enforce minimum and maximum length;
* Set password expiration period and credential rotation avoiding password reuse;
* Check the password against a set of breached passwords such as top 1,000 or 10,000 most common passwords which match the system's password policy;
* Avoid contextual string in the password (e.g., user id, app name);
* User can change password and requires for current and new password;
* Provide a password strenght meter to help users set a strong password;
* No password composition rules limiting the type of characters permitted, like upper or lower case or numbers or special characters;
* Consider MFA, preventing single point of failure.
