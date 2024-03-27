# Use a base image with Java and specify the version
FROM tomcat:8.0.20-jre8

# Set environment variables
ENV CATALINA_HOME /usr/local/tomcat
ENV PATH $CATALINA_HOME/bin:$PATH

# Create a directory for Tomcat
WORKDIR /usr/local/tomcat

# Download and extract Tomcat 9
RUN apt-get -y update 

# Copy the WAR file into the webapps directory
ADD target/web-application*.war /usr/local/tomcat/webapps/web-application.war

# Expose the default Tomcat port
EXPOSE 8080

# Start Tomcat when the container starts
CMD ["catalina.sh", "run"]
