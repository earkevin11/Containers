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

