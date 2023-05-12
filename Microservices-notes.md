## Microservices:

#### 1. Springboot services, 2. API Gateway, 3. Hystrix Dashboard, 4. Service Registry, 5. Zipkin Server, 6. Cloud Config Server.
* All the above concepts help us to identify how microservices work together. And how we can create the microservices from monolithic application. And we can get an idea how to create a resilient microservices using a circuit breaker. Zipkin, Sluth libraries for a distributed log phrasing. 

## Service Registry:
* All the Microservices will be connected to Service Registry. We can get an idea what are the different microservices available and the status of all the microservices.

## API Gateway:
* This is a gateway for all the API's that we have in our microservices. 
* So all the requests shouldn't be going directly to the microservices. They should be going from one API gateway, and from there they should be traversed according to the microservices URL pattern or whatever the other information we can give for that.

## Histrix dashboard(Histrix circuit breaker):
* Suppose any of the microservice is not working, so we should send a message to particular user who are trying to access it. 
* We need to create a timeout for particular API and call fallback method after particular time.
* By implemeting this Histrix dashboard, we can visualise how many microservices are failing and how many are running. 

## Cloud Config server:
* If we have multiple(Hundreds/thousands) microservices, there might some of the configurations that would be repeated for all the microservices. It's not a best practice to add same configurations in all the microservices. 
* So for that we will create a git repository and all our configurations save there, and we will create a Cloud config server which will read that git repository and it will give all the configurations to the all microservices connected to it. 

## Zipkin server:
* For distributed logging we will use Zipkin server.
* If there are multiple microservices, we should be able to identify which microservice is failing and where our request is traversing. So for that we will use Zipkin and Sluth libraries.
* We will create a Zipkin server, and then we will implement the Zipkin client and sluth libraries in all our microservices to implemet the distributed logging. 
* With this Sluth library we will be able to identify which of the services been called, what is trace id, what is the span id.
* For each service the trace id is unique. 

