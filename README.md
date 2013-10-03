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
λ ~/ tunnel sweater@memorici.de:22%/home/sweater/.ssh/id_rsa 22~22022
Running reverse SSH tunnel:
 * * * 
User:  sweater
Host:  new.memorici.de
Port:  21984
PubID: /home/sweater/.ssh/id_rsa
 * * * 
Local port:  22
Relay port:  21985
Target port: 21984
```
