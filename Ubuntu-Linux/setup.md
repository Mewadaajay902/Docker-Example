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



