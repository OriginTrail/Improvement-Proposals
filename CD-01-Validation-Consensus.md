## Simple Summary
### Proposal - Litigation: Validation Consensus
The documented litigation process for challenging the integrity of data stored on the Origin Trail Decentralized Network (ODN) involves several smart-contract executions on a separate distributed computing Network (Ethereum).
This proposal focuses on reducing the quantity of smart-contract calls by utilising the ODN to act as a pre-validator.

## Abstract
As decentralised solutions scale, it is important that they maximise their integrity and efficiency.
Using 3rd party systems - in Origin Trails case Ethereum smart contracts - for validation is a good way to test integrity of data stored by discrete nodes, however this comes at a cost which feeds directly into the 3rd party systems economy and therefore impacting on the solutions economy.
Utilising the ODN to perform the majority of these tasks increases efficiency through reduced fees, ensures integrity as more challenges can be presented to the network, and overall improves the utilisation of the network. 

## Motivation
Reduced Ethereum Gas fees for Data Creators and Data Holders, with potential for feeding the fees saved back into the ODN economy through an internal fee structure.

## Specification
The current documented process for litigation requires the Data Creator (DC) and the Data Holder (DH) execute a smart contract to test data integrity.
This process is actioned by the DC if it does not get a satisfactory response from the DH when challenged with a data block.

### Proposal:
This proposal would add a process into the current procedure between the DC’s check and the smart contract validation. 
The process would utilise the ODN nodes to validate the data block through a Validation Consensus, therefore reducing the number of smart contract calls and also mitigating against bad actors.

### Procedure Flow:
> DC: Data Block Request ----> DH: Data Block Return ---> DC: Validation Check ---> DC: Validation Fails ---> DC | DH : Broadcast  for Validators ---> Nodes reply and form Validator Pool (VP) ---> DC | DH: Send Data to VP for validation ---> VP: Returns Validation Consensus Score (%) ---> Validation Passes [END] / Validation Fails – Smart Contract Final Litigation

If the data returned to the DC does not pass their internal check, the data is passed into the ODN for Validation. 

The DC would first notify the DH of the Validation Consensus.

The DC and DH broadcast to the ODN requesting validation of data. DH’s respond to the request, offering their capacity to execute the required validation*.

A determined number of DH nodes are selected by the DC and DH, and the Validator Pool (VP) is agreed. 

Data is sent by both the DC and DH for validation to the VP, who check the data as per the documented litigation process.
If the returned result from the collective VP Validation Consensus is lower than 50%, the DH and DC are informed that there is a discrepancy and the process continues to smart contract for resolution and final litigation.

**A fee structure could be added to this to add to the ODN economy. This could be a fee paid at time of DC data creation. Any fees not used could be returned to the DC or used as a development pool.*

## Rationale
The RFC outlines the process of consensus on the ODN.
Further improvements to the proposal could be made by removing the DC’s authority to self-police the data. 
This would be done by checking data across replicated data nodes and taking action against bad actors, including DC’s attempting to game the system.

Another example would be a tiered node structure which would provide greater security to the overall network through .

## Backwards Compatibility
This improvement proposal is unlikely to be backward compatible and would be considered an hard fork, requiring all nodes to be updated.

## Test Cases
No test cases available at this time.

## Implementation
This RFC is a proposal and would need to be fully scoped before implementing.
