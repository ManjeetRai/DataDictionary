## Running on local:

1. Verify Java 17 Installation

2. java -version
 -if not java 17 installed use below commands
   sudo apt update
   sudo apt install openjdk-17-jdk

3. Verify Maven Installation
    mvn -version
 -if not installed
   sudo apt update
   sudo apt install maven

4. Build the Project
   mvn clean install

5. Run the Project
   mvn spring-boot:run

   


## Running using Docker

1. Build the Project
   mvn clean install

2. Build the Docker Image
   sudo docker build -t data-dictionary .

3. Run the Docker Container
   sudo docker run -p 8080:8080 data-dictionary




