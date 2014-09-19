vSRX Demo topology
==================

This vagrant file represents demo a simple topology JDDoS. It contains two clients and one server.

Client 1
--------

Client 1 in this scenario is our attacker. It will be executing attacks against the Server as well as client 1.

Client 2
--------

This client device will represent an unsecured host on the Internet. It is running Apache 2 with HTTP/HTTPS enabled and Bind 9.

Server
------

This server device will represent an secured host on the Internet. It is running Apache 2 with HTTP/HTTPS enabled and Bind 9.

vSRX
----

The vSRX will represent our device under test. It is configured in L3 routing mode and will route traffic between the client and the server networks.

```
+------------------+          +--------------------+        +------------------+
|                  |          |192.0.2.1/24        |        |                  |
|                  |          |                    |        |                  |
|  192.0.2.10/24   +-----+----+                    +--------+ 198.51.100.10/24 |
|                  |          |                    |        |                  |
|                  |          |     198.51.100.1/24|        |                  |
+------------------+          +--------------------+        +------------------+
     Client 1                         vSRX                         Server

```
