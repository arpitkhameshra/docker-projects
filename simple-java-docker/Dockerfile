#pull a base image which gives all required tools and libraries
FROM openjdk:17-jdk-alpine

#create a folder where a app will be stored
WORKDIR /app

#Copy the source code from your Host Machine to your container 
COPY src/Main.java /app/Main.java

#compile the application 
RUN javac Main.java

#run the appliucation 
CMD ["java","Main"]
