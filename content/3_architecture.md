## Architecture
{:#architecture}
This work presents a minimal 
architecture that can model the trust
flow requirements for automated
data integration in decentralized
networks of data stores.
This section is structured 
according to the requirements
presented above.

<!-- <br/> -->
(i) 
<!-- The data requirement -->
The first requirement is to enable 
the storage and retrieval 
of user age data with sufficient 
and verifiable proof of integrity.
<!-- is dependent on the modeling  -->
This relies on the ability to
model data with its associated 
metadata and the capability of 
the network to understand this 
model to enable discovery,
querying and verification of data.
<!-- What choices did we make? -->
<!-- 1. RDF to model data -->
For this purpose the Resource
Description Framework (RDF)
was decided upon
[](cite:cites Cyganiak:14:RCA).
<!-- Why RDF? -->
RDF provides the flexibility to
model requirements for data, 
associated metadata and policies
with interoperability in 
semantics on a Web scale 
through ontologies.
<!-- 2. VCs to model data authenticity as associated metadata -->
Here the Verifiable Credentials
(VC) specification [](cite:cites
Hartog:22:VCD) defines a protocol
for issuing and verifying signatures
on top of the RDF data, enabling 
straightforward storage and sharing
of verifiable data and 
authenticity in the network.
<!-- 3. Solid for identity and data storage. -->
To enable this storage and sharing,
the Solid protocol 
[](cite:cites sambra2016solid)
provides the functionality for 
storage and retrieval of resources
for personal data stores on the Web.

(ii)
<!-- Requirement -->
The second trust flow requirement is 
for users to trust their data stores
to enforce their preferences and legal 
requirements for data exchanges.
<!-- prevent manual review -->
To prevent falling back on manual
user review on the grounds of informed
consent for every interaction, 
as cookie banners tend to do 
[](cite:cites kretschmer_cookie_2021),
automating access where possible is 
key for scaling integration efforts.
<!-- Modeling requirement -->
This requires enforced policies to express 
user preferences and legal requirements 
for data sharing and usage 
covering the variety of use cases 
the network should support.
<!-- Other bases -->
Additionally, the coverage of 
legal bases such as vital interest 
or legitimate interest provide 
necessary alternatives to consent
under the GDPR regulation as
pathways to automating
data sharing [](cite:cites fierens_data_2024).
<!-- ODRL and DPV -->
To tackle these requirement we support 
the choice of the Open Digital Rights 
Language (ODRL) [](cite:cites Iannella:18:OIM) 
and the Data Privacy Vocabulary (DPV) 
[](cite:cites Esteves:24:DPV) to 
represent user preferences and legal
requirements for access to and usage of data.
<!-- backing up the claim -->
This follows the use of extended ODRL 
in IDS usage control architecture 
[](cite:cites noauthor_416_2023),
active research on alignment with GDPR
[] (cite:cites pandit_enhancing_2024)
and formalization efforts for evaluation engines.
<!--  -->
To combine ODRL capable policy evaluation engines
with separate storage mechanisms such as 
the Solid protocol, the User Managed Access
(UMA) [](cite:cites machulak_user-managed_2010)
protocol is used.
The protocol is based on decoupling
resource storage (Solid) 
and policy enforcement (ODRL + DPV)
and enables automating negotiation 
over policy requirements.

<!-- <br/> -->
(iii) 
<!-- Requirement of automated trust in usage -->
The final requirement poses that the
service can trust a successful retrieval
of data to provide sufficient information
on how the data can be stored and used 
in compliance with user preference
and legal regulation.
<!-- Policy instantiation! -->
This requires the requirements for access 
and usage of data that are modeled in the
policies enforced over the data to be
tied to the data and provided to the 
requesting party.
For this, we make use of policy instantiation,
<!-- todo: citation for policy instantiation? -->
where generic policy requirements are fixed 
for the interaction and instantiated
in a policy that models the agreed upon conditions
for access and usage of a selection of data
for that interaction.
<!-- Uses of these instantiations -->
These instantiated policies can now be used
by to validate usage of received data by 
services,
to automate validation of usage by auditing 
systems
and to keep track  user can keep track 
of data sharing and to withdraw consent 
for specific exchanges by users.
