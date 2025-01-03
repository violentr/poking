FROM tomcat:9.0.93-jdk21-corretto-al2


# Configure Tomcat manager by default
RUN mv /usr/local/tomcat/webapps /usr/local/tomcat/webapps2 && \
    mv /usr/local/tomcat/webapps.dist /usr/local/tomcat/webapps

# Copy custom configuration files into the image
COPY ./temp/tomcat-users.xml /usr/local/tomcat/conf/tomcat-users.xml
COPY ./temp/context.xml /usr/local/tomcat/webapps/manager/META-INF/context.xml

# Expose port 80
EXPOSE 80

# Start Tomcat
CMD ["catalina.sh", "run"]
