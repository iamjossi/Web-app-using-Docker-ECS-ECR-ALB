# Web-app-using-Docker-ECS-ECR-ALB

In this project, I designed and implemented an end-to-end cloud-native application deployment pipeline on Amazon Web Services (AWS). The primary goal was to containerize and deploy a web application, ensuring scalability, security, and efficient resource management.

**Key Steps and Achievements:**

1. **EC2 Instance Setup:**
   - Created an EC2 instance as a starting point for building the cloud-native application.
   - Configured SSH access to the instance for remote management.

2. **Docker Installation:**
   - Installed Docker on the EC2 instance, enabling containerization of the application.

3. **Docker Image Creation:**
   - Created a Dockerfile to define the application's environment and dependencies.
   - created an index.html file which serves as an entry point for my web application 
   - Built a Docker image from the Dockerfile.

4. **Amazon Elastic Container Registry (ECR):**
   - Established a private container image repository in Amazon ECR to securely store Docker images.
   - Configured the AWS CLI for ECR access, ensuring seamless interaction with the repository.

5. **IAM Roles and Policies:**
   - Created IAM roles to facilitate secure communication between AWS services.
   - Created ECR role with administrator access policy to enable me execute ECR tasks.
   - Created ECS role with ECS execution role policy for ECS service.

6. **Amazon Elastic Container Service (ECS):**
   - Defined an ECS task definition, specifying container configurations and resource requirements.
   - Created an ECS cluster to manage containerized applications.

7. **Amazon Elastic Load Balancer (ALB):**
   - Established an Application Load Balancer (ALB) to distribute incoming web traffic to ECS tasks.
   - Integrated the ALB with the ECS service for load balancing.

8. **ECS Service Configuration:**
   - Configured an ECS service, indicating the desired number of containers (scaling to 2 instances).
   - Attached the IAM role to the ECS task to ensure proper execution and access.

To be sure my application deployment was successful, I copied the DNS name of the ALB from the service I created, pasted it on a web browser and I can access my application. The docker file and index.html file used for this project is included in this repository.
