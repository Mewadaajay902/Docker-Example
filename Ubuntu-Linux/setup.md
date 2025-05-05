# Ubuntu-Linux Setup with Docker

This guide explains how to set up an Ubuntu environment locally using a Docker image.

## Step 1: Create a Directory for Storage

First, create a directory on your local system that can be used by the container for storage:

```bash
mkdir ubuntudatastore
```

## Step 2: Set Up Ubuntu Environment Using Docker

Run the below command to set up an Ubuntu environment locally using a Docker image:

```bash
docker run -dit \          
--name ubuntu-container \
--hostname ubuntu-dev \
--restart unless-stopped \
--cpus="2" \
--memory="4g" \
--mount type=bind,source=/Users/ajaymewada/tmp/ubuntudatastore,target=/data \
-v /var/run/docker.sock:/var/run/docker.sock \
-p 2222:22 \
-p 8080:80 \
--env TZ=Asia/Kolkata \
--env LANG=en_US.UTF-8 \
ubuntu:latest /bin/bash
```


## Step 3: Access the Ubuntu Container

Command to access the Ubuntu container:

```bash
docker exec -it "container ID" /bin/bash 
```

<img width="1046" alt="Screenshot 2025-05-02 at 5 06 14 PM" src="https://github.com/user-attachments/assets/c9476e39-0fe3-4067-a115-fe5e8174f8ac" />




