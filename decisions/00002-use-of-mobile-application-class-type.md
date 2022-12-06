# 1. Use of Mobile Application class type for Mobile Apps

_Date: 2022-12-05_

### Issue
***
There is not an established mechanism to classify mobile applications within the Intermountian Healthcare EA Metamodel.

Stakeholder has surfaced use case with following needs pertaining to managing Mobile Applications:
* Tracking security approval
* Tracking associated cost(s)
* Associating mobile applications with certain use cases and/or responsible owners
* Managing a centralized list of 'approved' Mobile Applications

### Decision
***
Mobile Application class type will be added to the EA Metamodel and used as the mechanism to store Mobile 
Application data.

### Status
***
Approved

### Group
***
Metamodel Class Types

### Assumptions
***
There seems to be no 100% correct way in which to account for mobile applications in current iteration of EA Metamodel.

This is due to multiple reasons:
* Regardless of classification, development resources will be required.
* Governance associated with Mobile Applications may or may not be different from pre-existing class types.
* Reporting on Mobile Applications changes depending upon the way in which the records are classified.

### Constraints
*** 
Development work associated with ServiceNow is currently sparse, as Intermountain prepares for new 'Greenfield' 
ServiceNow instance. Regardless of the decision, development work will be required.

#### If the Mobile Application Class is not used:
- We may end up stifling the flexibility provided by the out-of-box Ins-Pi class types to quickly meet the needs of new use cases.
- Creating reports of Mobile Application records becomes more complicated if they're not in their own class type.
- How the DXC Team responsible for managing mobile applications may be hindered, as data attributes Pre-Existing class types won't reflect their specific needs.
  - Impacts how the DXC team Manages the Data
  - Impacts the Data Quality not reflecting the specific needs of Mobile Application records 

#### If the Mobile Application Class is used:
- Other Metamodel Types will need to account for the relationship(s) it may have with the Mobile Application class type.
- The distinction between Business Application, Software Product, Software Program, and now Mobile Application may be confusing to users of UPM-X.

### Positions
***
2 Primary Positions

##### Position A. The Mobile Application Class Type Should be Leveraged
* UPM-X already has a Class Type specifically built for Mobile Applications
* The needs associated with managing Mobile Applications differ from those presented through other class types
* IT is rapidly transforming -- use of Mobile Applications will likely only increase; let's get ahead of it before we're forced to account for it
* Forms and other attributes will specifically pertain to Mobile Applications; avoiding the issue of an abundance of unnecessary columns/fields for Mobile Applications if they're classified elsewhere. 

##### Position B. An Existing Class Type should be used to account for Mobile Application records
* We haven't used other out-of-the-box UPM-X Class Types; Thus, we don't have to use something just because it's available
* Notating that a particular record is a mobile application could be notated through a 'type' attribute within an existing class type
* The more class types we add to our metamodel, the murkier the differentiation between existing class types become

### Argument
***
As above.

The model can account for this now, before the demand for tracking Mobile Application data potentially increases. 
By separating Mobile Applications into their own class type, the reporting (Data Quality) associated with those records
becomes much easier to govern and manage; as compared to the alternative option of managing these records from within
other class types.

### Implications
***
Resources will need to be secured in order to properly configure the Mobile Application class type. 

Metamodel documentation will need to account for the addition of the Mobile Application class type.

Relationships between the Mobile Application & other pre-existing Class Types need to be established and documented.

Current mobile applications loaded only account for attributes that may be specific to iOS-based Mobile Applications. 
Configuration of class type may need to be revisited if additional OS's are to be accounted for.

Data within this class type will be manually imported and/or added by DXC Staff. Enterprise Architecture may want to 
account for the possibility of this load eventually being automated, depending on how/if the volume of data changes 
over time.

### Related Decisions
***
Decision 1: Use Mobile Application Class Type to store Mobile Application data

Decision 1.A: DXC Staff will Manage/Govern Mobile Application Class Type Records in a manual manner for the meanwhile.

Decision 1.B: Mobile Application Class Type will have relationships with the following class types: Business Capability, Technical Capability, Business Application.

Decision 1.B.1: Relationship between Mobile Application and Business Capability is: Mobile Application > _provides_ > Business Capability; Business Capability > _is provided by_ > Mobile Application

Decision 1.B.2: Relationship between Mobile Application and Technical Capability is: Mobile Application > _provides_ > Technical Capability; Technical Capability > _is provided by_ > Mobile Application

Decision 1.B.3: Relationship between Mobile Application and Business Application is: Mobile Application > _is used by_ > Business Application; Business Application > _uses_ > Mobile Application

### Related Requirements
***
_Requirement 1: Managing Mobile Applications_ 

_Requirement 2: Reporting on Mobile Application Data_

_Requirement 3: Data Quality on Class Type_

_Requirement 4: Class Type Addition to Metamodel_

### Related Artifacts
***
_[EA Metamodel Wiki/Knowledge Documentation](https://teams.microsoft.com/l/entity/com.microsoft.teamspace.tab.wiki/tab::7c7d56ca-fb99-46e8-ac46-71368df0e073?context=%7B%22subEntityId%22%3A%22%7B%5C%22pageId%5C%22%3A73%2C%5C%22origin%5C%22%3A2%7D%22%2C%22channelId%22%3A%2219%3A84a8ab9c3aee4c859244a88840760d6e%40thread.skype%22%7D&tenantId=a79016de-bdd0-4e47-91f4-79416ab912ad)_

_[EA Metamodel Designer Diagram](https://intermountain.service-now.com/x_inpgh_des_designer.do?diagram_sys_id=a77904e1db3819506e11ee0c13961989&present=1)_

### Related Principles
***
_Example Principle: Forward Thinking Architecture_

_Example Principle 2: Out-of-Box Thinking_

### Notes
***
Because the decision-making process can take weeks, it may be useful to capture notes and issues that the team discusses
during the socialization process.