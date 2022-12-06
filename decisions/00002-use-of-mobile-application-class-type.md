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

Current mobile applications loaded only account for attributes that may be specific to iOS-based Mobile Applications. 
Configuration of class type may need to be revisited if additional OS's are to be accounted for.

Data within this class type will be manually imported and/or added by DXC Staff. Enterprise Architecture may want to 
account for the possibility of this load eventually being automated, depending on how/if the volume of data changes 
over time.

### Related Decisions
***
It's obvious that many decisions are related; these can be listed here. However, it has been found in practice, a 
traceability matrix, decision trees, or metamodels are more useful. Metamodel are useful for showing complex 
relationships diagrammatically (such as Rose models).

### Related Requirements
***
Decisions should be business driven. To show accountability, explicitly map your decisions to the objectivevs or 
requirements. You can enumerate these related requirements here, but it may be more convenient to reference a
traceability matrix. You can assess each architecture decision's contribution to meeting each requirement, and then assess
how well the requirement is met across all decisions. If a decision doesn't contribute to meeting a requirement, don't 
make that decision.

### Related Artifacts
***
List the related architecture, design, or scope documents that this decision impacts. 

### Related Principles
***
If the enterprise has an agreed-upon set of principles, make sure the decision is consistent with one or more of them. 
This helps ensure alignment along domains or systems.

### Notes
***
Because the decision-making process can take weeks, it may be useful to capture notes and issues that the team discusses
during the socialization process.