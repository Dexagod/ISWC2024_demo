## Architecture
{:#architecture}

In this work, we present a minimal 
architecture that can translate the
required trust flows to automate 
trust flows that combines
that enables the requirements defined in the use case based on 
open Web standards: 
(i) Decentralized storage of data that includes metadata such as provenance, signatures as sufficient proof of data integrity.
(ii) Modeling, instantiation and enforcement of dynamic governance requirements through policy negotiation and instantiation.
(iii) Proving use and misuse of data through the exchange of instantiated policies.

In the proposed architecture, as displayed in [REFERENCE FIGURE!], 
the network is setup around an adaptation of the 
User Managed Access (UMA) protocol. [CITE]
This protocol is designed to provide a centralized
control point for authorization 
(the Authorization Server component)
to manage data stored their different
storage locations (the Resource Server component).

In the following sections, 
we go in depth over the different components.


### Data Integrity in decentralized storage and exchange 
<!-- 
* Raw Data Now <-> Trust Envelopes! 
* We propose an architecture that captures the above requirements for data integration and trust flow modeling
* We implement this above an extension of the Solid data storage protocol with UMA. '
-->


<!-- Introduction -->
The modeling of data and its associated metadata 
forms the foundation of digital data ecosystems.
This defines the both the capabilities of the system 
and the capabilities of the data itself.
The capabilities of discovering, querying and enforcing governance
requirements for specific selections of data rely on the understanding
of the underlying modeling of the data and metadata.

<!-- Use case -->
The use case defined above poses the requirement that the
system architecture must enable the automated integration 
of user age in a way that provides
sufficient proof to trust the integrity of the data.
<!--  -->
Deconstructing this requirement, we find the following sub-requirements.
The data needs to be modeled in a way that can be understood in the network.
To provide sufficient proof for trusting the integrity of the data, 
additional context must be stored with the data in the form of provenance 
information and encryption methods that can tie the trust in real world entities
to this data and provenance information.
<!--  -->

<!-- Data spaces -->
<!-- say something about IDSA connector architecture? -->

<!-- Proposed architecture -->
In our minimal reference architecture, 
the choice is made to use RDF [CITE] as the modeling language 
for both the of data and metadata.
Where the semantics described in RDF about data allows
both for alignment through the semantics or explicit mapping
between context in data or querying, 
JSON-LD forms a middle ground for JSON-based architectures to provide 
a straightforward mapping from internal data to RDF.

To model the requirement of establishing proof of data integrity,
we make use of the Verifiable Credentials Specification [CITE].
This specification defines a standardized representation for
adding a combination of cryptographic signatures and provenance information
to data in JSON or JSON-LD format.

As the storage mechanism, we make use of the Linked Data Platform [CITE]
specification. This specification defines a Web interface mimicking
a file structure through URI semantics. Using this structure, we can store
the verifiable credentials as `https://<base_URL>/credentials/<credential_name>`.
The Solid Type Index mechanism [CITE] can be used to link the type of the 
credential to the URL where the credential is stored to enable discovery.

We note some shortcomings of this approach.
The use of Verifiable Credentials as the modeling mechanism 
for data, provenance and signatures imposes some restrictions
on the storage system, as these credentials must be stored as 
individual entries in the storage because their RDF representation
clashes when combined in an RDF datastore. They natively only
support simple provenance and signature information and are not
extensible. Another limiting factor is that they
only allow JSON and JSON-LD as format for the data and context. 
Note that the Solid LDP storage mechanism allows for any kind
of resource content, though this will then not support this modeling
of provenance and signatures.

<!-- 
Furthermore, we take some assumptions that we will address in future work.
* alignment on data using mappings
* derived resources based on queries -->

<!-- Modeling metadata / context -->

<!-- Verifying data + identifiers -->

<!-- Add the requirement as well of keeping track of data sharing? -->
<!-- 
The storage and sharing of data and associated metadata forms the foundation of digital data ecosystems.
The ecosystem choices on how data can be registered and how associated information can be linked
define the capabilities for sharing, discovering and integrating the available data.
In this aspect, we see a divergence in how this is approached.

At the 2009 Ted talk, sir Tim Berners Lee led the charge for 
"Raw Data Now"[CITE!](https://www.w3.org/2009/Talks/0204-ted-tbl/#(15)),
a rally for access to data on the Web to push innovation.
European data spaces initiatives [CITE!!] follow these ideals 
in the form of digital marketplaces for the Web.
Using a connector architecture, these data space initiatives
facilitate the integration of existing sources by registering 
their data offerings in the catalogs of the connectors in the network. [CITE]

On the other hand, we see the requirement for highly integrated systems
that focus on maximizing integration of data in the network.
For many use cases that need to comply to strict legal requirements,
parties need to trust that data is correct
and that they are using data correctly. [CITE RubenV no more raw data].
At the forefront here are digital wallet initiatives [CITE EUROPE, Blockchain wallets, ...]
that focus on strong protection and storage of data that maximize interoperability 
through rigid standards for modeling and formatting in their networks. 
This maximizes the potential for automated integration of these data points in the network. [CITE?] -->




### Authentication and authorization

The second requirement for the designed system is that data governance can be automated. 
This automation relies on the capabilities of clients to negotiate with the 
governance mechanisms protecting the data for access to and usage of selections of data.
Additionally, this mechanism should support some sense of dynamic decision making, 
so that not every time a new client comes to the data store, a manual review has to
take place, as this would present us with the same situation that 
cookie banners currently present in the Web environment. [CITE]

<!-- Modeling policies for access and usage -->
The enforcement of governance in decentralized data spaces
in term relies on the capability to model the requirements
for this enforcement in a way that can be understood by the
system.
We envision the requirements that need to be modeled
to start out as user preferences that are chosen from
smart default options and based on a user profile.
However, these should have the capability to scale with
legal requirements such as vital interest in case of
emergencies allowing the sharing of personal data
with certified emergency services. [CITE vital interest GDPR!!]
In addition to requirements modeling access to data,
the capability to model how data can used for processing
or storage after acquisition is essential to represent
user preferences and legal requirements.

<!-- ODRL model and enforcement  -->
To tackle these modeling requirement we support the choice
of the Open Digital Rights Language (ODRL) as the modeling 
language of choice to represent requirements for access to
and usage of data. [CITE ODRL]
<!-- todo: something about Abstract Policies?? -->
This follows the use of ODRL in the data spaces architecture. [CITE]
Active research on alignment with GDRP regulation using
ODRL and DPV is also ongoing [CITE], and a formalization 
effort for the outcome of evaluation engines is also 
in progress. [CITE]
Upon requesting a resource located on the Resource Server
as defined in the architecture overview [REF IMAGE!], 
the requesting party is redirected to the Authorization 
Server endpoint. 
<!-- claim negotiation --> 
Through this authorization endpoint, the requesting party
negotiates with the endpoint on the requirements for 
access to the requested data.
<!-- todo: something here about usage negotiations  -->


<!-- Policy instantation -->
Once the Authorization server has received enough
information to grant access to data, 
the relevant policies are instantiated 
into a single policy for the data exchange.
This instantiated policy contains the 
relevant and public access conditions
and the usage conditions under which 
the data exchange has taken place.
This instantiated policy is returned
to the requesting party together with 
an access token giving access to the data, 
encrypted in a way that can prove 
this instantiated policy was provided 
by this authorization server.






### Usage agreements and auditing flows
The policy instantiation mechanism combines
the public access requirements such as duration
with the usage requirements of the data.
These usage requirements, encrypted by the 
authorization server, form the agreement
under which the data was provider to the
requesting party.
This contains the information such as the 
purposes for which data may be processed and
the duration for which data may be used.
These instantiations are stored at the 
authorization server, and exchanged with the
requesting party in the data negotiation protocol.
The authorization server can make use of these 
instantiated policies as cached access grants
that shortcut the negotiation protocol for 
subsequent requests for the same data selection.
Additionally these form a log of the live
data exchanges and can allow the data owner
to withdraw consent or prove misuse of data.
The receiving party must store these instantiated
policies as proof of the agreement under which
data was retrieved. These can automate internal
data processing systems to only include data
for which the processing is valid according to
the usage agreement.
Additionally these can automate parts of
auditing processes, as these agreements can
be automatically processed and verified.


<!-- Intro -->

<!-- Usage Agreements -->

<!-- Auditing capabilities -->
<!-- 
* Three trust flows
  * Data origin - VCs
  * Access control - UMA + ODRL
  * Usage control - instantiation + agreement + auditing

* Glue to hold system together
  * UMA
  * Storage - Solid
  * data representation - VCs
    * Credentials Issuer
  * Authorization system 
    * ODRL engine
    * Claim negotiation
  * Usage Agreement

* Automated auditing capabilities

* (Web store client) -->
