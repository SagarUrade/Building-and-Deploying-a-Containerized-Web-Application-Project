### Building and Deploying a Containerized Web Application

- Step 1: Create a ec2 instance 
          example - I have create EC2 using terraform, ssh into it.
          C:\Users\Sagar Bhai\Desktop\Devops_note\Docker\Docker Project\Docker Project SS\EC2Instance.png


- Step 2: Install Docker in Ec2.
          refer here - https://get.docker.com/

### Lets bring up a Website in a container.

- Step 3: -Fashion Free CSS Template refer here:  https://www.free-css.com/free-css-templates/page296/little-fashion

         - Free CSS Templates : https://www.free-css.com/free-css-templates

- Step 4:  mkdir website

           cd website

           wget https://www.free-css.com/assets/files/free-css-templates/download/page296/little-fashion.zip

           unzip little-fashion.zip

     - **move this folder to html location in      webserver 2127_little_fashion**
    - **mv 2127_little_fashion /var/www/html/fashion/**          

- Step 5: Webservers: nginx

- Step 6: Create a file called as Dockerfile
         C:\Users\Sagar Bhai\Desktop\Devops_note\Docker\Docker Project\docker file.txt
          

- Step 7: Now to build the  docker image lets use docker build command.
          
          docker image build -t fashion:1.0 .

          C:\Users\Sagar Bhai\Desktop\Devops_note\Docker\Docker Project\Docker Project SS\Docker process.png

           
- Step 8: Now lets view the images

         C:\Users\Sagar Bhai\Desktop\Devops_note\Docker\Docker Project\Docker Project SS\Docker Image.png

- Step 9: Now lets build the container with this image
          
          docker container run -d --name web1 -P fashion:1.0 

          C:\Users\Sagar Bhai\Desktop\Devops_note\Docker\Docker Project\Docker Project SS\container process.png


- Step 10: Copy public ip / port no / fashion
          
          example: http://13.126.143.105:32768/fashion/

          C:\Users\Sagar Bhai\Desktop\Devops_note\Docker\Docker Project\Docker Project SS\Website host.png
        