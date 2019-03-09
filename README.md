# DRAM Customer Return System


### Credits
### Project members of Institute of Systems Science, National University of Singapore:
* Ong Boon Ping

---

### [ 1 ] Project Title

DRAM Customer Return System



---

### [ 2 ] Abstract

In a particular DRAM manufacturer, QA is in charge of receiving customer returned parts. While QA is able to re-run the testing flow, it is rely on test engineering department to provide further technical intent of the failing parts. 
After gathering the info, QA will decide further industrial action to be taken based on the finding of customer returned part.


---

### [ 3 ] Features


The system is designed for the QA to record the return part details and it will trigger test engineers to check on the parts.
At the beginning, QA will key in the part detail and the test re-run (on the part) result.
Test Engineer will check whether the past data is available and the part is passing. 
If the part is passing re-run, the analysis will be continued by test engineers. If it fails re-run and past testing record still in test engineering database, if the testing flow remain unchanged, the part will be considered as degrader. However, if it fails re-run while the testing flow has been changed after the parts goes to customer, it will be defined as guardbanded parts. QA will get the result and enter the comment for degrader/guardbanded parts.

However, if the parts passing the re-run, analysis continues. In common, customer system can get too hot and so the parts fail. Thus, temeprature range is extended for the test flow. If it fails, the parts is considered to be a customer violation case. If it pass, the returned part will be going for further analysis with stringent test flow. If it pass the stringent flow, sales team should discuss with customer on whether the customer system has limitation or abusing the parts. 
If it fails stringent test, the test engineer will run the stringent test on limited samples. If the stringent test will results in fallout (>1%), the sales representative should discuss with customer in getting higher performance parts and specify new requirement. If the overkill fallout is acceptable, QA can close the case while TE can continue to implement the test flow. 


---

### [ 4 ] User Guide

download pre-built virtual machine from http://bit.ly/iss-vm

Open jbpm-server
(Running with jbpm server 7.16 zip file in case 7.12 is not working. Zip file is available at https://drive.google.com/file/d/1yTv9wW7Coz9b0nzkhAZgn1Q02Xl7EOOK/view . Run ~/jbpm-server/bin/standalone.sh)

start iss-vm

open terminal in iss-vm

$ git clone https://github.com/optimusium/ISSProj

Getting zip file. Unzip the zip file.
https://github.com/optimusium/ISSProj/blob/master/DRAMCustomerReturn.zip

Create space "individual". Import the project to space "individual" in Business Central using the following path
file:///home/iss-user/DRAMCustomerReturn

Create user (with password the same)
QA
TestEngineer
DRAMSales

---

### [ 5 ] Report Link
https://github.com/optimusium/ISSProj/blob/master/IndividualReport.docx


