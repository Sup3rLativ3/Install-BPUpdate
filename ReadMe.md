Install-BPUpdate
=================

This script will check to see if an incremental Best Practice data update has been released today and if so download and install it.


 Parameters
 -------------- 
 **-Date**  
  	_Not Required._  
   _Pipeline not accepted._   
   _Named Position._   
   _No Wildcards._   
  	This fills the filename to download. You can use this if you are searching for a specific date.
  
 **-Destination**  
  	_Not Required._  
   _Pipeline not accepted._   
   _Named Position._   
   _No Wildcards._   
  	Sets the download directory for the data update file. By default this will be C:\BPUpdate
  
 **-DownloadURL**  
  	_Not Required._  
   _Pipeline not accepted._   
   _Named Position._   
   _No Wildcards._   
  	This is the URL to download the file from. This also includes the filename.
  
 **-OutFileName**  
  	_Not Required._  
   _Pipeline not accepted._   
   _Named Position._   
   _No Wildcards._   
  	This sets the name to download the file as.
    
 **-EventSource**  
  	_Not Required._  
   _Pipeline not accepted._   
   _Named Position._   
   _No Wildcards._   
  	This sets the name of the source for event viewer logs.

-------------------

Use the "Install BP UPdate.xml" to create a scheduled task. Be sure to replace DOMAIN\ADMIN with the credentials you want to use.

-------------------
Exmaple usage
-------------- 

  `.\Install-BPUpdate.ps1`
        This will run the script with default. The download will be downloaded to with the original filename to C:\BPUpdates
    
  `.\Install-BPUpdate.ps1 -OutFileName "BPUPdate.exe"`
  	    This will run the script with defaults but set the saved filename to "BPUpdate.exe" (without the quotes).
   
   `.\Install-BPUpdate.ps1 -Date "170105" -Destination "C:\Temp" -OutFileName "TempBPUpdateFile.exe" -EventSource "PS BP Update Script"`
       This will attempt to download the update from 2017/01/05 and write the file "TempBPUpdate.exe" to "C:\Temp" and if an error occurs it will write the source as "PS BP Update Script"
