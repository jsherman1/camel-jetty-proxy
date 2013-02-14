camel-jetty-proxy
=================

Example Camel route which uses a Jetty Endpoint as a Proxy

This project contains two routes using a Jetty Endpoint as a Proxy
One route demonstrates an issue using chunked=false on teh Jetty Endpoint
which is being tracked by 

    http://fusesource.com/issues/browse/MR-696
    
The other route is using the default chunked=true which is working as expected

To run this router either embed the jar inside Spring
or to run the route from within maven try

    mvn camel:run
    
Once the run is running the endpoint can be invoked by hitting:

    http:localhost:8199/test
    http:localhost:8299/test

For more help see the Apache Camel documentation
