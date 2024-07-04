## Conclusion
{:#conclusion}
This paper and the accompanying demonstrator effort
shows a minimal architecture decentralized networks of
data stores that enables the required trust modeling
defined by the guiding use case using open Web specifications:
<!-- trust in data and context -->
(i) 
Combining RDF and VCs to model data
and context as verifiable credentials
with Solid for the storage and retrieval
of resources over the Web
provides the capabilities for  
services in the network to automate
the retrieval and integration of
trusted data in the network.
<!-- trust in enforcing policies -->
(ii) 
The use of ODRL and DPV to model
user preferences and legal requirements
in system policies with UMA to enable
negotiation over policy requirements
provides the capability to automate
negotiation for data access while
providing users with trust in the
enforcement of user and legal requirements.
<!-- trust in retrieved data -->
(iii)
Policy instantiation models the access 
and usage requirements for data exchanges.
This enables services in the network 
to trust their compliance with user
preferences and legal requirements 
when processing data retrieved through
automated interactions in the network.

Future iteration on this architecture is planned to include the following considerations:
(i) Minimizing data requirements through selective disclosure
and expanding the scope of its associated metadata beyond integrity.
(ii) Formalizing requirement modeling and negotiations
to include data context requirements such as integrity
and usage requirements such as processing needs.
(iii) Formalizing policy instantiation mechanisms for ODRL and DPV.