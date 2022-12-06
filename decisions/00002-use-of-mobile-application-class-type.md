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
Lis the positions (viable options or alternatives) considered. These often require long explanations, sometimes even
models and diagrams. This isn't an exhaustive list. However, you don't want to hear the question "Did you think about...?"
during a final review; this leads to loss of credibility and questioning of other architectural decisions. This sections 
also helps ensure that options' of others were heard; explicitly stating other opinions helps enroll their advocacy in 
the decision. 

### Argument
***
Outline why the position was selected, including items such as implementation cost, total ownership cost, time to market, 
and required development resources' availability. This is probably as important as the decision itself.

### Implications
***
A decision comes with many implications, as the REMAP metamodel denotes. For example, a decision might introduce a 
need to make other decisions, create new requirements, or modify existing requirements; pose additional constraints to ]
the environment; require renegotiating scope or schedule with customers; or require additional staff training.
Clearly understanding and stating the implications of the decision will be very effective in gaining buy-in and creating 
a roadmap for architecture execution.

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