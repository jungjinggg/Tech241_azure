# How to create Virsual Machine on Azure

select create > Azure virtual machine

![azure_vm_create](az_vm_create.png)

### Create a virtual Machine > Basics

1) create **virtual machine name**  
2) **image:** select *Ubuntu Pro 18.04 LTS - x64 Gen2* >
3) **size**: *Standard_B1s*

![vm_create_basic](vm_create_basic.png)

4) Username: *adminuser*
5) SSH public *key source: Use existing key stored in Azure*
6) Stored key: *select key that stored in Azure*
7) Public inbound ports: *Allow selected ports*
8) Select inbopund ports: *select HTTP(80) and SSH(22)*

![vm_create_basic2](vm_create_basic2.png)

### Create a virtual Machine > Disks

change OS disk type: *Standard SSD*
 
![vm_create_disks](vm_create_disks.png)

### Create a virtual Machine > Networking

change Subnet: *default*

![vm_create_network](vm_create_network.png)

### Create a virtual Machine > Tags

add Name: *Owner*
add Value: *Parichat*

![vm_create_tags](vm_create_tags.png)

### Create a virtual Machine > Review + create
Use this page to review and check everything before create a virtual machine

![vm_create_review](vm_create_review.png)



