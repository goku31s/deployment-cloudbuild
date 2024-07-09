FROM openjdk:16-jdk-buster

# Set non-root user for security best pracitices
USER root

# Download and install Tomcat 10.1.25
RUN wget -O /tmp/apache-tomcat.tar.gz https://downloads.apache.org/tomcat/tomcat-10/v10.1.25/bin/apache-tomcat-10.1.25.tar.gz \
    && tar xfz /tmp/apache-tomcat.tar.gz -C /opt \
    && mv /opt/apache-tomcat-10.1.25 /opt/tomcat \
    && rm /tmp/apache-tomcat.tar.gz

# Set permissions
RUN chmod -R 777 /opt/tomcat

# Expose Tomcat default port
EXPOSE 8080

# Start Tomcat
CMD ["/opt/tomcat/bin/catalina.sh", "run"]
