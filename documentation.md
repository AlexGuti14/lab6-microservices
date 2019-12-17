# Lab6 - Microservices - Documentation

**1)** The two microservices are running and registered (two terminals, logs screenshots).
---
You can see the first account Microservice up and registered:
![Image 1](img/account2222.png "Microservice account up and running")

You can see the web Microservice up and registered:
![Image 2](img/web.png "Microservice web up and running")

---
**2)** The service registration service has the two microservices registered (a third terminal, dashboard screenshots)
---

![Image 3](img/registration.png "Eureka dashboard with 2 MS registred")


---
**3)** A second account microservice is running in the port 4444 and it is registered (a fourth terminal, log screenshots).
---

The port in file [application.yml](accounts/src/main/resources/application.yml) has been changed. (port: 4444)

You can see the second account Microservice up on port 4444 and registered:

![Image 4](img/account4444.png "Accounts Microservice up and running on port 4444")

Dashboard in Eureka:

![Image 5](img/registration_2.png "Accounts Microservice up and running on port 4444")

---
**4)** A brief report describing what happens when you kill the microservice with port 2222. Can the web service provide information about the accounts? Why?
---

Kill first account on port 2222:

![Image 6](img/account2222_kill.png "Kill account in port 2222")

Dashboard in Eureka:

![Image 7](img/registration_kill2222.png "Kill account in port 2222")

When the first microservice listening on port 2222 is killed and you try to retrieve information about the accounts, you can still get it, because the application swaps the microservice and gets the information from the microservice listening on port 4444, which is a replica.

You can see the demo application and the information retrieved from the microservice on port 4444:

![Image 8](img/webInfo.png "Demo Aplication Web Server")

![Image 9](img/webInfo2.png "Accounts Info from microservice on port 4444")

You can see Logs of second accounts microservice on port 4444:

![Image 10](img/account4444_2.png "Logs of second accounts Microservice on port 4444")