## logger-eureka-server

[![Build Status](https://travis-ci.org/JudeNiroshan/logger-eureka-server.svg?branch=master)](https://travis-ci.org/JudeNiroshan/logger-eureka-server)

This is the netflix-eureka server which is used for service discovery
between [audit-server](https://github.com/JudeNiroshan/audit-server) ↔️ 
[logger-app](https://github.com/JudeNiroshan/logger-app). 

Why we need an Eureka server? 🤷🏼

In a real-world production infrastructure, it is likely to deploy multiple
instance of a same application to serve the in-coming traffic. In our case, 
it is probable that we may want to scale the number of gRPC server instances 
AKA logger-apps to server our incoming requests. 

In such a situation, we need to dynamically lookup where our logger-app 
instances are deployed in order to call RPC methods. Eureka server act 
as a middle man who keep track of URI information for logger-app instances.

![Alt text](docs/overview.jpg?raw=true "Title")

logger-app [eureka registration done here.](https://github.com/JudeNiroshan/logger-app/blob/master/src/register-app.js)

#### How to run 🏃🏽‍♂️
 
 - clone the repository to your machine [`https://github.com/JudeNiroshan/logger-eureka-server.git`]
 - move to `logger-app` [`cd logger-eureka-server`]
 - execute `./mvnw install`
