# simple_write_behind_caching

The goal of this project is to demonstrate a simple write behind caching mechanism with RabbitMQ and Memcached.

For the need of this demo, the use case is simple: we want to add a user to the database.

Our user object consists of a LastName, FirstName and Age.

The goal of a write-behind caching strategy is to process the write directly to the caching system first, and then asynchronously write to the database. 
In comparaison to a write-through caching strategy, the write-behind strategy improves the write performance (the user doesnt have to wait for the write to complete(i.e for the write to be processed by the database).

This simple project will then go multiple stages where i'll first convert all the pieces of the system architecture into microservices, then we'll add a k8s layer onto it, then i'll migrate everything to AWS.
