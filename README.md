## logger-eureka-server

This is the eureka server which is used for service discovery
between audit-server and logger-app applications. 

logger-app application instances will register to this 
eureka server upon the start-up. Therefore, audit-server 
can easily lookup for the logger-app instances which are 
registered to this eureka server.

logger-app [eureka registration](https://github.com/JudeNiroshan/logger-app/blob/master/src/register-app.js)
