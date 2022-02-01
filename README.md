# ECS



*********************************************************************************
Sample of dockerize app and uplode this image to container on AWS service (ECS).
*********************************************************************************


1. Build an app on node.js - like server.js file
2. Add Dockerfile and define it (npm install and expose the app on port 3000)
3. Build the image by this command : docker build -t my-exmple-app-docker .
4. Run this command for check the image: docker images
5. Connect to AWS account and upload this image to ECR by instructions of aws (click the "View push commands" button) you need to tag the image by something like this command: 
docker tag my-exmple-app-docker:latest 137520671512.dkr.ecr.us-east-1.amazonaws.com/my-exmple-app-docker:latest
6. And push the image to ECR by this command:
 docker push 137520671512.dkr.ecr.us-east-1.amazonaws.com/my-exmple-app-docker:latest
7. Finally we need to define continer and upload this image (using the ECS service)