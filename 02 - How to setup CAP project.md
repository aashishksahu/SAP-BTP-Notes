## How to setup CAP project 

### Follow the commands below to create a project
  ```bash
  cds init the-project # initialize a project
  cd the-project       # move to the project folder
  npm i
  cds add mta
  cds add hana
  cds add xsuaa
  cds add sample       # or create your own schema and services
  ```

### Update template generators package
 ```
 npm i -g @sap/generator-fiori
 ```

### Add managed approuter

1. Right click the newly generated `mta.yaml` and select `Create MTA Module from Template` 
    
2. Select `Approuter Configuration` and press `Start`

3. Select your HTML5 application runtime `Managed Approuter`

4. Enter a unique name for the business solution of the project | Enter a unique ID e.g. `<your-mta-id>-service` from step 1.3

5. Do you plan to add a UI? `Yes`

6. Overwrite bookshop/xs-security.json? -> `Overwrite`

### Create a SAP Fiori application

1. Open the command palette `View` -> `Find Command` -> `Fiori: Open Application Generator`
2. Select a template
   ![image](https://github.com/user-attachments/assets/953380c2-57c5-41b1-abba-d54d3108c2de)
3. Select appropriate data source
   ![image](https://github.com/user-attachments/assets/95a7d176-422e-49e8-960e-570be1d3c220)
4. Select appropriate entity
   ![image](https://github.com/user-attachments/assets/99a06e6d-8a0c-4823-9c46-3be0968407a3)
5. Select project attributes, select the options (highlighted below in yellow) to add MTA deployment config and Fiori Launchpad config
   <img width="923" alt="image" src="https://github.com/user-attachments/assets/32a6e05f-8d4a-4186-95b6-dc14fa38ae23">
6. Select an appropriate destination (**Note:** Wait for some time for all destinations to show up, don't select DIRECT_SERVICE_BINDING)
   ![image](https://github.com/user-attachments/assets/519bc46e-a08d-4400-b5cb-1538fd1b8d84)
7. Fill out the details for Fiori Launchpad config and finish

### Deploy the project

```
npm run build
npm run deploy
```

# Links

[Approuter Configuration - SAP Community.pdf](https://github.com/aashishksahu/SAP-BTP-Notes/blob/caf4ed13b49a358abd431a1f9f0b258cc2239629/Res/Approuter%20Configuration%20-%20SAP%20Community.pdf)

