## What is this project?

This project *cas-overlay-demo* has been created to test the CAS server and the CAS services management webapps (version >= *4.0*) using the *Maven overlay* mechanism: [http://jasig.github.io/cas/4.0.x/installation/Maven-Overlay-Installation.html](http://jasig.github.io/cas/4.0.x/installation/Maven-Overlay-Installation.html).  
It's composed of two overlays:

- the *cas-overlay-server-demo* module is the CAS server webapp
- the *cas-overlay-management-demo* module is the CAS services management webapp.

## Deploy

To start quickly, build the project:

    cd cas-overlay-demo
    mvn clean install

and start the two web applications with jetty:

    cd cas-overlay-server-demo
    mvn jetty:run

To test,

- call the [http://localhost:9001/cas-management](http://localhost:9001/cas-management) url to access the CAS services management webapp
- be redirected to CAS server and authenticate (username: jleleu, password: jleleu)
- be redirected back to the CAS services management webapp, being successfully authenticated.

## Manual deployment

You can also deploy manually these two web applications in your favorite web applications server:

- cas-overlay-server-demo on http://localhost:9001/cas
- cas-overlay-management-demo on http://localhost:9001/cas-management.
