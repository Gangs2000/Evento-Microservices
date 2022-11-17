# Evento-Microservices

Evento Java Microservices. It's kinda bookmyshow application which allows user to book their seats for any show at any time. Upon successful booking seats, user will be notified via email. If needed, user can also cancel their seats before 3 hours of show time.

**Implemented Microservice :**

1. Registration Service
2. Event Details Service
3. Authentication Service
4. Booking ticket Service
5. Email-Notification Service
6. Payment Service


**SPRING-NETFLIX-EUREKA-SERVER**

All microservices have been registered with Spring Eureka server. Eureka server is nothing but a cloud server where we can register all microservices as a client.
Spring Eureka act as a server and all other microservices act as a client.

**API-GATEWAY**

Api-Gateway has been implemented for abstraction purpose. The use case of API-GATEWAY is not to expose original port number of each microservice. So whenever client sends a request to client first it will hit API-GATEWAY and check whether the given endpoint has been implemented in any microservice, If it finds the method further the client request will be redirected to that method to perform necessary action.

**BOOTSTRAP-SERVER**

Instead of keeping all properties files in respective microservices, bootstrap allows to keep all the prop files remotely ( Here we have kept prop files int GITHUB page ).

**REGISTRATION-SERVICE**

As name suggests it allows end user to register their profiles in our application further they can book tickets for particular events/shows. Basically two types of registration is available one is for normal people and another for organizers those who can schedule their shows/events by registrating their theatre properties.

**EVENT-DETAILS-SERVICE**

This microservice will keep all details about shows/events such as Date, Time, Location, Duration, Cast/Crew, Languages and Format etc. This end point can only be accessed by organizers, people who have not registered as a Organizer can't use this microservice.

**AUTHENTICATION-SERVICE**

Authentication purpose is used to authenticate end users for identification, Unregistered people can't use our application, Spring Security JWT has been implemented for security purpose.

**BOOKING-TICKET-SERVICE**

This service will help end user to book seats for a show/event by picking date, time and location. Cancellation option is also available to cancel booked seats, but it has to be done 3 hours before show timing.

**PAYMENT-SERVICE**

Payment service is being used for transaction purpose. Upon successful transaction end user will get a details about booked seats in their profile. We have used Razorpay payment application for collecting amounts. For cancellation, amount will be refunded to user account.

**EMAIL-NOTICIATION-SERVICE**

This service will trigger an email to user upon successful booking seats and cancellation seats. JavaMailSender package has been used.

**FEIGNCLIENT CONCEPT**

This package helps to connect another microservice, basically we can call rest endpoints which is implemented in another microservice. It acts as a bridge to connect microservice.

**RABBITMQ**

RabbitMq is also know as Message broker communication, which basically transfer data from one service to another service. Purpose of using RabbitMq is to ensure for data persistent. If one user service is down, the listener can't consume data, Meantime data will be persisted in Queue, once microservice is up and running queue will consumed by another microservice.

**Technologies used**

1. Core Java
2. Spring boot framework
3. Docker for virtualization
4. CI-CD GitLab
5. AWS - CLOUD

**HappY Coding**



