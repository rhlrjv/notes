# Ports and Adapters Design Patterns. 
** The Clean Architecture **

---

> I'd like to share thoughts and some code illustrating the "Ports and Adapters" technique for separating out your application from your app delivery details (REST / Rabbit / etc).  I know Mike G wants to share some thoughts here, too.  
> Gabe

---

https://blog.8thlight.com/uncle-bob/2012/08/13/the-clean-architecture.html

Outside in

  * Web, Devices, DB, External Interfacesj
  * Controllers, Presenters, Gateways
  * Use Cases
  * Entities


Use DTO ( Data Transfer Objects ) to transfer data from the inside layers to the outside.

The outer layers can only depend on its corresponding lower layer

---
