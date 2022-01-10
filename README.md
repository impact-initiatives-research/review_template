## What the project does  
The project looks at the cleaning performed on a dataset. It is heavily oriented for data collected
through KoBoToolbox.  
It currently performs the following checks on the dataset itself and on the cleaning:  
  * On the dataset  
    - Duplicates (on a single identifier)  
    - Possible Personal Identifiable Information  
    - Duration of the surveys  
    - Shortest path taken  
    - Outliers (using standard deviation rule)  
    - Other and text column that could possibly be changed  
    - Deletions between raw and clean data
  * On the cleaning
    - If the values from the clean data correspond to the value of the cleaning log.  
    - If some changes from the raw and clean data have been performed and no entry in the cleaning could be found.  

## Why the project is useful  
This markdown will create a default report to verify the data cleaning. It aims to support the users by
running a couple of standard checks. 

## How users can get started with the project  
You will need the following packages:  
  - tidyverse  
  - knitr  
  - kableExtra  
  - write_xlsx (default package used to write output and keep the different formating)  
  - cleaninginspectoR (default package to performed some checks) **devtools::install_github("impact-initiatives/cleaninginspectoR")**  

The only section that should be change is the block starting with "#The only section that should be changed."  
  - You have to read your raw and clean dataset, your cleaning log and the deletion log.  
  - You will have to give information about the unique identifier for your data for each of dataframe named above.  
  - You will have to give information about your cleaning log, especially the names of the variable for the question, old and new value.  
  - You will have to change if to add or remove a type of check by changing it TRUE or FALSE. It allows to get some control on how the
  markdown will be knitted in case you don't have all relevant documents or if you think some part are irrelevant.  
  
## Where users can get help with your project  
Try to reach out to me directly.  

## Who maintains and contributes to the project  
So far only me will be maintaining the project. Feel free to fill in an issue on the github page to bring
but to my attention or to request new features.
