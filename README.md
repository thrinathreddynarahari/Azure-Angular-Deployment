# Deploying Angular Application in AZURE

Hi Dev's , To deploy an angular app in Azure follow the below procedure.

## Generate Build

Create a build folder for your angular project by using the following command.

```
ng build --prod
```


## Create a ResourceGroup / Use existing Resource group and a Web App

Select the resource group if it existes or create a new resource group in Azure portal create a new Web App.

![This is an image](https://raw.githubusercontent.com/thrinathreddynarahari/Azure-Angular-Deployment/main/webapp_generation.png)

Then Select the RuntimeStack as "Node 16 LTS"

![This is an image](https://raw.githubusercontent.com/thrinathreddynarahari/Azure-Angular-Deployment/main/runstack.png)

Select all the options as shown in below image and click on create.
![This is an image](https://raw.githubusercontent.com/thrinathreddynarahari/Azure-Angular-Deployment/main/overall_settings.png)



## Further steps

Open the search bar on the left and search for advanced tools and click on go.
![This is an image](https://raw.githubusercontent.com/thrinathreddynarahari/Azure-Angular-Deployment/main/next_steps.png)

This will redirect you to another window called "Kudu Services"

## Kudu Services

Kudu Services should look like this

![This is an image](https://raw.githubusercontent.com/thrinathreddynarahari/Azure-Angular-Deployment/main/debug_console.png)

Open the "Debug Console" tab and select "CMD"

Next window should appear as below:
![This is an image](https://raw.githubusercontent.com/thrinathreddynarahari/Azure-Angular-Deployment/main/cmd_site.png)

Then go through the Folder structure

site>>wwwroot>>hostingstart.html

Then delete the hostingstart.html .
![This is an image](https://raw.githubusercontent.com/thrinathreddynarahari/Azure-Angular-Deployment/main/deleting_hosting_html.png)

After deleting the hosting.html then drag and drop the project folder inside the dist folder into the window
dist>> ~projectname~
![This is an image](https://raw.githubusercontent.com/thrinathreddynarahari/Azure-Angular-Deployment/main/uploading_dist.png)

## Path configuration
After uploading the project dist folder then open azure portal and use the right side serch bar and search for "Configuration" and click on the configuration option    
![This is an image](https://raw.githubusercontent.com/thrinathreddynarahari/Azure-Angular-Deployment/main/seRCH_COFIGURATION.png)
This open the following window then open the path mappings Tab.
![This is an image](https://raw.githubusercontent.com/thrinathreddynarahari/Azure-Angular-Deployment/main/PATH_MAPPINGS.png)

Then scrool to 'virtual applicatons and directories' and edit the virtual path
Append the project dist folder name to the path 
![This is an image](https://raw.githubusercontent.com/thrinathreddynarahari/Azure-Angular-Deployment/main/adding_virtual_path_root.png)


Save the changes that you have made
![This is an image](https://raw.githubusercontent.com/thrinathreddynarahari/Azure-Angular-Deployment/main/save_the_settings.png)
## Finish
Open your webapp and you can find all the detalis of your webapp.
![This is an image](https://raw.githubusercontent.com/thrinathreddynarahari/Azure-Angular-Deployment/main/final.png)

Open the url . 
Congratulations you have deployed your Angular Application in AZURE.

