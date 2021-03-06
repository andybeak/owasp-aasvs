4.4 Authorisation of direct object references
=============================================

Verify that access to sensitive records is protected, such that only authorized objects or data is accessible to each user (for example, protect against users tampering with a parameter to see or alter another user's account).

Levels: 1, 2, 3

General
-------

    A direct object reference occurs when a developer exposes a
    reference to an internal implementation object, such as a file,
    directory, database record, or key, as a URL or form parameter. An
    attacker can manipulate direct object references to access other
    objects without authorization, unless an access control check is in
    place. For example, in Internet Banking applications, it is common
    to use the account number as the primary key. Therefore, it is
    tempting to use the account number directly in the web interface.
    Even if the developers have used parameterized SQL queries to
    prevent SQL injection, if there is no extra check that the user is
    the account holder and authorized to see the account, an attacker
    tampering with the account number parameter can see or change all
    accounts. This type of attack occurred to the Australian Taxation
    Office's GST Start Up Assistance site in 2000, where a legitimate
    but hostile user simply changed the ABN (a company tax id) present
    in the URL. The user farmed around 17,000 company details from the
    system, and then e-mailed each system. This was a major
    embarrassment to the Government of the 17,000 companies with details
    of his attack. This type of vulnerability is very common, but is
    largely untested in current applications.

-  `OWASP: Top 10 2007-Insecure Direct Object
   Reference <https://www.owasp.org/index.php/Top_10_2007-Insecure_Direct_Object_Reference>`__

