# Fiori Monitor
Fiori Monitor App description

# Installation Steps
1.  Go to the transport folder and download the transports to your local machine.
2.  Log on to the SAP Gateway system
3.  Go to transaction CG3Z. You will be given a prompt with two input fields. Put these values in sequence and execute:
    
    File 1
    Source file on front end: <File path in your local machine>/K900728.S4H
    Target file on application server: /usr/sap/trans/cofiles
    
    File 2
    Source file on front end: <File path in your local machine>/R900728.S4H
    Target file on application server: /usr/sap/trans/data
  
    File 3
    Source file on front end: <File path in your local machine>/K900730.S4H
    Target file on application server: /usr/sap/trans/cofiles
    
    File 4
    Source file on front end: <File path in your local machine>/R900730.S4H
    Target file on application server: /usr/sap/trans/data
  
 4. After all the files are succesfully installed, go to transaction STMS_IMPORT. Navigate to Extras -> Other Requests -> Add from the menu. A popup will appear. Select S4HK900728 from the Transport Request Value List. Click on continue. The request will appear on the import queue. 
 5. Select the request and click on the 'Import Request' (Ctrl + F11) button. Wait for the installation to be complete. 
 6. Repeat steps 4 and 5 but this time select request S4HK900730 from the transport request list.
 7. After the installations are complete, we need to configure the app in the Fiori Launchpad. Steps for these can be found in the blog https://www.mindsetconsulting.com/how-to-setup-sap-fiori-launchpad/
 
 # Validation 
 1. It may be possible that that Odata service is not active. In which case, go to /IWFND/MAINT_SERVICE and activate the ICF node for /MINDSET/FIORI_MONITOR_SRV.
 
 

