# Set the base image to use
FROM openjdk:8-jre
#This line adds the productcatalogue-0.0.1-SNAPSHOT.jar file from the target directory in your project to the Docker image and names it app.jar.
ADD target/productcatalogue-0.0.1-SNAPSHOT.jar app.jar
#This line adds the product-catalogue.yml file from your local directory to the Docker image and names it app-config.yml.
ADD product-catalogue.yml app-config.yml
# Expose the port that the application will listen on
EXPOSE 8020
#This line specifies the command that will be executed when the Docker container is started. 
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","app.jar", "server", "app-config.yml"]
