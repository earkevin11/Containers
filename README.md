# Containers


# Why do we need containers?
- Companies will spend a lot of money install applications on multiple machines.
- To save compute costs, and to prevent one application from affecting another application on the same machine, we use containers like Docker.
- They're isolated units that contain an application. 
- Machines can have multiple containers. There won't be any application conflict because the container isolates them.


# Applications on their own machines
- The applications will not affect each other since they are isolated by virtual machines
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/172237243-cf28ae52-610c-420a-b998-cf9dc56c570d.png" height="90%" width="90%" alt="review of vnets and VMs"/>

<p/>

# Example of why companies use containers
- Imagine having 2-3 applications on one virtual machine 
- Sometimes, an installation or an update can affect each other and cause the other to crash
- To combat that, admins will use containers
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/172234121-1aee58aa-163c-4b6f-b2f2-ebd7838b7bc9.png" height="90%" width="90%" alt="review of vnets and VMs"/>

# Containers diagram
- This is for visual learners like myself
- Containers like dockers would be used to isolate multiple applications installed on a single virtual machine 
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/172236880-f1d186e5-ac14-4777-b617-c763e1c7e875.png" height="90%" width="90%" alt="review of vnets and VMs"/>
  
<p/>



# Deploying Docker instance on Linux Machine
- Create a Linux Machine
- Download and install Putty


# Why are we using Putty?
- Putty is used to SSH into a Linux machine from a Windows-based machine
- Enter the Public IP of the linux vm created and SSH into the VM

<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/173869736-3f199e1f-f486-45f6-918f-f99e539c85da.png" height="40%" width="40%" alt="review of vnets and VMs"/>
  
<p/>

# Enter the following commands and install Docker
- Go to the website - https://docs.docker.com/engine/install/ubuntu/ - here users can insert the following commands to install Docker

<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/173877905-d21fd935-9902-442d-a61c-885a634a34dd.png" height="105%" width="105%" alt="review of vnets and VMs"/>
  
<p/>

# Confirmation of Docker installation
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/173882454-fb041333-0f12-4ef9-b682-f35f8aa996b8.png" height="65%" width="65%" alt="review of vnets and VMs"/>
  
<p/>


# 141 - Follow video to build the image
- The container will be built from the image
- Once admin runs the commands, the Linux VM shoulde run the container with the help of the Docker Engine on the Linux VM

# Copy the public folder - created by Udemy Instructor - we're creating an Image
- Then we're going to create a container from the image
- Copy the contents in the folder onto the linux vm using WinSCP
- Run the commands to create the image from the contents

<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/173903424-65b9a00d-9a00-4167-80de-398d69459e11.png" height="65%" width="65%" alt="review of vnets and VMs"/>
  
<p/>

# Open up port 80 because now users will need to access the Linux VM to view the container
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/173903621-4853b78a-75ee-4e15-a1a9-9077c1ca0da2.png" height="125%" width="125%" alt="review of vnets and VMs"/>
  
<p/>

# Successful container on Linux VM
- The application is now being ran as a container on the Linux VM.
- Everything is running as a container with the help of the Docker Engine

<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/173903920-7189f17e-f4ad-4dca-bb5d-13cf0c2c7f33.png" height="65%" width="65%" alt="review of vnets and VMs"/>
  
<p/>


# Purpose of Azure Container Registry
- This service can be used to hold your images on Azure.
- One can also host images on DockerHub
- Other developers can run a container on another vm based on that image

# Create the Azure container registry
- This Container Registry is within Azure and will host the images for developers
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/173929181-0550f15f-e4a3-4e2f-b99b-789f0ed5a377.png" height="65%" width="65%" alt="review of vnets and VMs"/>
  
<p/>


# Push the image from the Linux VM onto the container registry
- Now we must push the image from the Linux VM to the Azure Container Registry - appregistry2031

# Follow these commands # 144
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/173930985-b578a600-6e03-4897-9d17-288f19ed539c.png" height="65%" width="65%" alt="review of vnets and VMs"/>
  
<p/>

# Successful login to Azure CLI
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/173931228-781fe4d9-cfcf-4ace-ae63-f02b5e0593ed.png" height="65%" width="65%" alt="review of vnets and VMs"/>
  
<p/>

# When logging into Azure Container Registry
- Ensure in the commands that the registry is the same as what was created
- appregistry2031

<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/173931228-781fe4d9-cfcf-4ace-ae63-f02b5e0593ed.png" height="65%" width="65%" alt="review of vnets and VMs"/>
  
<p/>

# After pushing the image, users should see the image we named "my app" in the repository
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/173932876-a3ed81d0-521a-48b1-83c3-186ce1d00804.png" height="100%" width="100%" alt="review of vnets and VMs"/>
  
<p/>

# my app image should appear in the Azure Container Registry
- Developers and Admins can now create containers using this image in the registry

<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/173933027-367bfc87-35c0-4590-94ef-ed994cb96b19.png" height="85%" width="85%" alt="review of vnets and VMs"/>
  
<p/>


# Container Instance
- Create a container instance using the Container Registry
- It will have an public IP where users can access it via the internet


# In order for Azure Container Instances to authenticate to pick up an image from the repository
- Admins must enable admin user in "Access Keys" settings
- One service does not trust each other automatically. Security is very important.
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/173934720-bf92dcd9-5944-4620-845a-e0925916e952.png" height="125%" width="125%" alt="review of vnets and VMs"/>
  
<p/>




