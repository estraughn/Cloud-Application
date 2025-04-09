# Launching a Cloud Application Using Containerization

# Objective
 I will build a Docker container image, upload it to IBM Cloud Container Registry, and deploy an application on cloud using a serverless technology called IBM Code Engine. The application is called Guess the Capital it is a web application that asks you to guess the capital of a country from 4 choices.

 # Tools Used 
 - Docker
 - IBM Cloud
 - IBM Code Engine

 # Steps

 1. First I opened up a terminal in the provided interactive development environment(IDE) and verified that Docker was installed and that it was the lastest version, I then verified the latest version of IBM cloud as well.
    ![Screenshot 2025-04-09 142305](https://github.com/user-attachments/assets/2899da06-7f22-4504-a62e-dc2c7bab4773)

2. I then navigated over to IBM Code Engine and booted it up and then started the code engine command line interface(CLI).
    ![Screenshot 2025-04-09 143006](https://github.com/user-attachments/assets/20629f05-3d64-4e20-a3e1-4e5d52186cfe)

3. Next I ran the highlighted command in the CLI to clone the Git repository that contains the starter code needed and created a directory called fyidw-guess-the-capital to store the downloaded contents.
   ![Screenshot 2025-04-09 143913](https://github.com/user-attachments/assets/fb20d80f-f8a2-47da-93ce-c1c0220de81e)

4. I then changed directories over to the newly created one and ran an ls command to verify that all of the correct files downloaded from the git repository.
   ![Screenshot 2025-04-09 144238](https://github.com/user-attachments/assets/0a88f065-4f5b-40bd-87af-67c1563201a4)

5. I then created an http server using the command python3 -m http.server in the CLI. Once the server was hosted I visited the created site and tested my work.
   ![Screenshot 2025-04-09 144617](https://github.com/user-attachments/assets/c164d94a-6e92-4b04-804a-06d8d9463f88)

6. I then opened Docker and created a docker file with the following commands entered to copy all the contents of the application over into the container.
   ![Screenshot 2025-04-09 145325](https://github.com/user-attachments/assets/83be1d81-4dd4-4ec6-a006-2029e073494d)

7. I then used the command shown in the following image to create an image file from the previously created docker file.
   ![Screenshot 2025-04-09 150119](https://github.com/user-attachments/assets/bc42df16-774d-4331-9cca-a2ad4d8814e4)

8. Next I ran the command docker images to verify the details of the created docker image within the directory. Then I ran the commad shown in the following image to host the application from the created Docker image, and proceeded to test the application again as done in previous steps.
   ![Screenshot 2025-04-09 150545](https://github.com/user-attachments/assets/d86403c4-a9d4-4a2a-a531-787647f3cf7c)  ![Screenshot 2025-04-09 150626](https://github.com/user-attachments/assets/45081036-a859-4d43-b637-730e3ca80497)

7. Now it is time to upload my application to IBM cloud. Using the command in the image below I again created the Docker image from the Docker file and added tags to the image so it can be pushed to IBM Cloud's container registry under my namespace.
   ![Screenshot 2025-04-09 152116](https://github.com/user-attachments/assets/2c874d49-9042-4f9d-9e2e-816640c67592)

8. Next I pushed the Docker image to the IBM cloud and then deployed the application using the commands in the following image.
   ![Screenshot 2025-04-09 152333](https://github.com/user-attachments/assets/782cb703-b7d6-4371-883b-c1912099d051)

9. Now that the application was uploaded to the cloud it was time again to verify that everything was working as it should so first I ran the following command in the CLI: ibmcloud ce application get --name guess-the-capital. which provided me with the follwing output
  ![Screenshot 2025-04-09 152717](https://github.com/user-attachments/assets/2451bcb8-5933-4586-a545-c3272c989062)

10. Fianlly, I took the provided URL from the last output and visited the site from my browser(Google Chrome) and tested the application from there to verify the application worked.
    ![Screenshot 2025-04-09 153140](https://github.com/user-attachments/assets/60ebb307-b83f-4e89-8600-8bcfd8d0ddd6)










