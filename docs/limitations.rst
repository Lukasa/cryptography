Known security limitations
--------------------------

Lack of secure memory wiping
============================

`Memory wiping`_ is used to protect secret data or key material from attackers
with access to uninitialized memory. This can be either because the attacker
has some kind of local user access or because of how other software uses
uninitialized memory.

Python exposes no API for us to implement this reliably and as such almost all
software in Python is potentially vulnerable to this attack. However the
`CERT secure coding guidelines`_ consider this issue as "low severity,
unlikely, expensive to repair" and we do not consider this a high risk for most
users.

.. _`Memory wiping`:  http://blogs.msdn.com/b/oldnewthing/archive/2013/05/29/10421912.aspx
.. _`CERT secure coding guidelines`: https://www.securecoding.cert.org/confluence/display/seccode/MEM03-C.+Clear+sensitive+information+stored+in+reusable+resources
