# GoRest_API_test

## Pre-requisite:
1. You may clone the whole repository to local
2. Install newman with command prompt terminal (will require to install node.js)

       npm install -g newman

## To run the postman collection:
    newman run <collection_file_path> -e <environment_file_path> 

Replace the `<collection_file_path>` with the collection file path

Replace the `<environment_file_path>` with the environment file path

**[Windows]** select the file, then press `ctrl + alt + C` to copy the file path
  
**[VSCode]** select the file then press `shift + alt + C` to copy the file path

## Description for each collections:
1. `GOREST.postman_collection`
   
   This collection that have pre-request script that able to generate random inputs, every run with different random inputs.

2. `GOREST_REQUIRED_ITERATION_DATA.postman_collection`
    
   This collection will need to run with iteration data that also will able to find in the IterationTestData folder. 

   To run this collection:

        newman run <collection_file_path> -e <environment_file_path> --iteration-data <iteration_data_file_path>

    Replace the `<iteration_data_file_path>` with the `.csv` data file path

3. `GORESTV2.postman_collection`
   
   This collection used to demostrate simple postman collection automate test cases assertion. (have pre-request script that able to generate random inputs)

4. `GORESTV2_REQUIRED_ITERATION_DATA.postman_collection`
   
   This collection is the required iteration data input version of `GORESTV2.postman_collection`

   To run this collection:

        newman run <collection_file_path> -e <environment_file_path> --iteration-data <iteration_data_file_path> 

*Change the data in the `gorest_create_user_data_set.csv` file for different result, as the data in might be used to create user. 

Hence, the result might hit the same response code `422 Unprocessable Entity`