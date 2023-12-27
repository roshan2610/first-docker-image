# first-docker-image
Demo docker repo for practice
<br><br>
Steps to execute docker- (We are using ubuntu flavor)<br>
<br>
Step 1: update terminal<br>

        SUDO apt update -y<br>
        Install Docker<br>
        SUDO apt install docker.io -y<br>
        <br>
        To check the status of docker<br>
         SUDO systemctl status docker<br>
        make sure that status is active if not - <br>
        SUDO systemctl restart docker <br>
        Now rather than using SUDO we will add our user(ie ubuntu) to the docker group<br>
        SUDO usermod -aG docker ubuntu
        <br>
Step 2: Now, login with DOCKER HUB credentials<br> 

        docker login<br> 
       Give docker hub username and password<br> 
        <br>
        Now, build our image<br>
        docker build -t docker-image-name . <br>
        Here docker-image-name will be our docker image<br>
        . specifies the path of our image ie current path<br>
        
Step 3: To check the image is present or not<br>

        docker images<br>

Step 4: Now, push the image to DOCKER HUB<br>

        docker push roshan09/first-docker:latest<br>
        Here latest is the tagname

Step 5: Run the image<br>

        docker run -it roshan09/first-docker:latest

Congratulations!!! You can see your application is running now!


