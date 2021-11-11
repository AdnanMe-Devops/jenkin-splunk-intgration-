# jenkin-splunk-intgration-
Create a Jenkins CICD Pipeline to Build a Docker Image with Splunk Integration

integrating Jenkins with Docker provides  a robust CICD method for building and packaging runnable containers. Building and deploying  docker containers is only half the challenge. Once they are in production, have to monitor and assess their operational performance. Splunk can provide you with this capability, through its support for enterprise-grade monitoring, logging, and diagnostics collection.

In this project will launch a Jenkins and Splunk CICD and monitoring environment using Docker containers on a provided EC2 instance and will then configure a Jenkins build pipeline to build, compile, and package a sample Java servlet web application into a runnable Docker image. The Jenkins build process will create the Docker image using a Dockerfile. The build process integrates Splunk logging into the Docker image, by installing the Splunk Forwarding Agent at build time. At runtime, the docker container will then have the ability to publish runtime logging information into the Splunk service. 


Objectives
Install and configure a Jenkins and Splunk CICD and monitoring environment using Docker containers
Configure Jenkins with the Gradle plugin to perform the core build and packaging for a sample Java servlet web application
Configure Jenkins with the Docker plugin for automated docker container build artifact management
Create and set up a Jenkins build pipeline using a Jenkinsfile stored within a GitHub repo
Launch a custom-built Tomcat Java servlet web application docker container, complete with Splunk logging integrated using the Splunk Forwarding Agent
Use the Splunk administration web console to search and report on collected and aggregated runtime data points emitted from custom Tomcat Docker container


steps
A single EC2 instance, named cicd.platform.instance, which will have a public IP address attached

Use Docker Compose to launch the following Docker containers:
Jenkins
Splunk
Socat
Using a browser, administer and configure Jenkins - installing the required plugins. Connectivity to Jenkins will be done via the cicd.platform.instance Public IP address 
Using a browser, administer and configure Splunk. Connectivity to Splunk will be done via the cicd.platform.instance Public IP address 
Create a Jenkins build pipeline and configure it to build a sample Java servlet web application hosted on GitHub, with the build artifact being a Docker image hosted on the cicd.platform.instance
Execute the Jenkins build pipeline and confirm that it has completed successfully, registering the resulting Docker image hosted on the cicd.platform.instance
Spin up the newly-created Docker image containing the Tomcat-hosted sample Java servlet web application
Generate sample user activity within the sample Java servlet web application - this will result in usage traffic being sent to the Splunk service
Use the Splunk administration console to search and report on the collected usage patterns
