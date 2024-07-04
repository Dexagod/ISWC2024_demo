## Architecture
{:#architecture}
In this work, we present a minimal 
architecture that can model the trust
flow requirements for automated
data integration in decentralized
networks of data stores.
This section is structured 
according to the requirements
presented above.

<br/>
(i) 
<!-- The data requirement -->
The first requirement for the network
is supporting the storage and retrieval 
of user age data with sufficient 
and verifiable proof of integrity.
<!-- is dependent on the modeling  -->
This requirement centers around the 
modeling of data with its associated 
metadata and the understanding
of this modeling in the network.
<!-- which makes many essential functions possible -->
Based on this understanding, 
the data can be discovered or
specific selections can be queried,
authenticity can be verified,
and claim requirements can be
enforced on said authenticity.

<!-- What choices did we make? -->
<!-- 1. RDF to model data -->
To model knowledge in the network, 
the RDF framework is used.
This modeling framework enables
the modeling of knowledge, associated
metadata and policies as quads
[](cite:cites Cyganiak:14:RCA).
<!-- Why RDF? -->
It combines flexibility in modeling
knowledge with interoperability in 
semantics through ontologies and
enables scaling this knowledge
beyond individual networks.
<!-- 2. VCs to model data authenticity as associated metadata -->
In addition to modeling information
providing data authenticity, 
a specification is required 
that enables integration and
verification of this information.
The Verifiable Credentials
(VC) specification [](cite:cites
Hartog:22:VCD) is a W3C recommendation
that defines the issuing and verification
process of credentials containing RDF data.
<!-- Why VCs? -->
These verifiable credentials 
containing both data and proof 
of authenticity can be easily 
stored and shared in the network.
<!-- 3. Solid for identity and data storage. -->
Finally the Solid protocol 
[](cite:cites sambra2016solid)
provides functionality for 
storage and retrieval of
resources over the Web.
<!-- Why Solid LDP? -->
<!-- todo: this part was weak! -->


<!-- <br/> -->
(ii)
<!-- Requirement -->
The second requirement needs users
to trust the governance mechanism
of their data stores to model and
enforce their preferences and legal 
requirements in a data exchange.
<!-- prevent manual review -->
To prevent falling back on manual
user review on the grounds of informed
consent for every new interaction, 
as cookie banners do on the Web 
[](cite:cites kretschmer_cookie_2021),
automation is a key requirement for
scaling integration efforts in the network.
<!-- Modeling requirement -->
This implies that the policies that 
are enforces must be able to express 
user preferences and legal requirements 
for data sharing and usage 
for the variety of use cases 
the network should support.
<!-- Other bases -->
Additionally, the coverage of 
other legal bases such as vital 
interest of legitimate interest
under the GDPR regulation also
provide pathways to automating
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
[](cite:cites noauthor_416_2023)
active research on alignment with GDPR
<!-- todo: cite!!! -->
and formalization for evaluation engines.
To evaluate the policies in the network,
we make use of the User Managed Access
(UMA) [](cite:cites machulak_user-managed_2010)
protocol to separate the Solid resource
storage from an external authorization server
and provide negotiation capabilities to
a parties requesting data.
This authorization server enforces 
the ODRL+DPV policies set on the user
data store by comparing the access 
requirements to the claims provided
with a data request, and indicating 
missing claims. This forms the basis
for the dynamic negotiation process.


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
by parties retrieving data in the network to
validate their use of data according to these
policies. Similarly auditing systems can 
automatically validate usage of data based
on these policies in the services they audit.
Finally, the user can keep track of their 
data sharing and withdraw consent for 
specific data sharing interactions.
