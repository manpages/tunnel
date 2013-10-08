tunnel
======

SYNTAX
---

Make a reverse SSH tunnel to the local machine from ``rhost``'s sshd listening to port ``rport``.
Login at ``rhost`` as ``user`` using private key located at ``full_path_to_id_rsa``.
Connect to the local sshd listening to port ``lport``.
Relay this connection on the ``rhost`` at ``relay_port`` so that you can ``ssh -p relay_port localhost`` to get to local machine from ``rhost``.

```
tunnel user@rhost:rport%full_path_to_id_rsa lport~relay_port
```

All elements are required.

EXAMPLE
---

```
λ ~/ tunnel sweater@memorici.de:12345%/home/sweater/.ssh/id_rsa 23456~34567
Running reverse SSH tunnel:
 * * * 
User:  sweater
Host:  memorici.de
Port:  12345
PubID: /home/sweater/.ssh/id_rsa
 * * * 
Local port:  23456
Relay port:  34567
```
