# 1. Use Mobile Application class type for Mobile Apps

Date: 2022-12-05

## Status
Accepted

## Context
EA Metamodel was evaluated to determine how to best classify Mobile Applications. Specifically, if the out-of-box
Mobile Application class type provided through UPM-X should be leveraged or pre-existing class types like Software Product.
Either option would require some form of customization as Software Product's current attributes don't align 1:1 with 
attributes required to capture and store data associated with Mobile Applications. However, there has been 0 work 
performed on the Mobile Application class type, and thus it would still require development work to modify certain fields.

Mobile Application data currently reside in InTune for inventory purposes. These data will be filtered down to only those that are iOS-based, 
then DXC Staff will manually import Mobile Application records.

The primary needs of the Stakeholder were to:
* Track security approval
* Track associated cost(s)
* Associate particular Mobile Applications with particular use cases and/or owners
* Manage a centralized list of 'approved' Mobile Applications

## Decision
The Mobile Application Class will be used to store records associated with Mobile Apps.

## Consequences
* Adding class type to EA Metamodel may cause confusion for users
* Current iteration of Mobile Application class type will only account for iOS-based applications due to use case
* Resources will need to be put towards creating a governance structure that best supports the enablement of use case.