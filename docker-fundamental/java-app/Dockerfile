#Getting Base image from dockrhub (first layer of automation in which java already installed)

FROM openjdk:11 

#Working Directory where all code will be kept

WORKDIR app/

#copy the code in the current directory of container (Hello.java is your system and . is our container) 
COPY Hello.java .

#Compile Code
RUN javac Hello.java

#Run Java Compiled code (2nd is class name/ file name)
CMD ["java","Hello"]
