# Blob storage 

There are different ways to create blob:
* Azure portal
* Azure CLI (command line interface)
* Azure Powershell

To check if azure CLI working on git bash run:
	`az`
Every single command using azure CLI start with `az`

1) To log in
    
    `az login`
    
    *When login don’t share anything with id* 

2) To create az storage
    
    `az storage account create --name tech241parichatstorage --resource-group tech241 --location uksouth --sku Standard_LRS`

3) List storage account
   
    `az storage account list --resource-group tech241`

    Display in a table

    `az storage account list --resource-group tech241 --query "[].{Name:name, Location:location, Kind:kind}" --output table`

4) Create a container

    `az storage container create --account-name tech241parichatstorage --name testcontainer`

5) Upload a blob
   1) Create a test file 
   2) Run
        
        `az storage blob upload --account-name tech241parichatstorage --container-name testcontainer --name newname.txt --file test.txt --auth-mode login`

6) Check if the blob is there

    `az storage blob list --account-name tech241parichatstorage --container-name testcontainer --output table --auth-mode login`

7) Change access level

    Azure storage account -> Container -> Change access level -> Change: public access level to *Blob (anonymous read access for blobs only)*
