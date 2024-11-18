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

2. Module name: uniquemodulename (make sure its unique in your organisation)

3. Namespace: com.hostname

4. Select `Yes` to `Add deployment configuration`, ensuring the newly generated MTA file is selected, refer to next step `Target Name`

5. Select `Yes` to `Add FLP configuration`, refer to next step `Overwrite` for input params, this is required for Launchpad to show your application tile

6. Follow the next steps and complete the wizard


### Deploy the project

```
npm run build
npm run deploy
```

# Links

https://github.com/aashishksahu/SAP-BTP-Notes/blob/main/Approuter%20Configuration%20-%20SAP%20Community.pdf

