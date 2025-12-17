[//]: # (Source: https://www.jetbrains.com/help/idea/link-job-to-changelist-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:31:24)

## Specify search parameters

Use the controls in this area for specifying various criteria to limit the search output. Follow the Perforce jobs [syntax rules](http://www.perforce.com/perforce/doc.081/manuals/cmdref/jobs.html). The specified values are joined in the generated command line query via the `AND` operation.

At least one of the fields should be filled in.

Item| Description  
---|---  
Job name pattern| In this field, type the desired job name search pattern.  
Status| Use this drop-down list to specify the status of the job you are looking for. The available options are: 

  * * \- when this option is selected, all the jobs that match the remaining search criteria are displayed, regardless of their job statuses.
  * Open
  * Closed
  * Suspended

  
User name pattern| In this field, specify the search pattern or the exact name of the user who created the desired job.  
Date before/Data after| Use these fields to specify the time period the desired job is created in. The appropriate formats are `yyyy/mm/dd` or `yyyy/mm/dd:hh:mm:ss`.  
Description pattern| In this field, type the desired job description search pattern.  
Search| Click this button to start searching for jobs that match the specified criteria.  
  
If you specify Status as the only criterion and select this option, all the jobs that are currently present on the Perforce server will be retrieved.
