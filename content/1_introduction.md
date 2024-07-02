## Introduction
{:#introduction}

<!-- A move for making data available -->
In a 2009 Ted talk [](cite:cites berners-lee_tim_2009), sir Tim Berners Lee called
for "Raw Data Now" as a driver for data innovation on the Web.
<!-- Data sharing initiatives -->
Recent initiatives such as European Data Spaces 
[](cite:cites braud_road_2021) have followed in this direction,
developing protocols that enable interoperable digital marketplaces
on the Web where data can be shared.
<!-- Web platforms thrive on collecting and INTEGRATING large amounts of data -->
In competition are the Web platforms 
that found enormous success 
over the last two decades, 
the majority of which can be 
attributed to the collection 
of large volumes of data and 
the integration of said data 
with their provided services.
<!-- Automated integration -->
This focus on automated integration
is crucial when making the translation
from Web platforms to decentralized 
networks of data stores.
<!-- integration relies on trust flows -->
Web platforms enable such automated 
integration through the internal modeling
of trust flows in a way that provides sufficient
guarantee for users to trust their preferences
and legal requirements are enforced and for
services to trust their compliance to the
above requirements and the authenticity
of the integrated data.
<!-- todo: the above might need a final rewrite -->
<!-- So we need to translate these trust flows! -->
In this work, we present a concrete 
network architecture based on Solid 
[](cite:cites sambra_solid_nodate)
and User Managed Access  sufficient
requirements for users and services to 

such as data authenticity, access control
and data usage. 
[](cite:cites machulak_user-managed_2010) 
that enables the translation of these trust 
flows to a decentralized network of data 
stores based on open Web specifications.
<!-- References -->
A running demonstrator and accompanying 
screencast of the proposed architecture
can be found on the [Github project page](https://github.com/SolidLabResearch/trust-exchange-demo).









<!-- Decentralization and data sharing -->

<!-- Decentralization efforts for data storage gave gained a lot of traction recently.
Where decentralized data storage and sharing has its roots in the early days of the Web
through protocols such as torrent [CITE], these lacked the ability to model the required
trust flows to handle sensitive data. -->

<!-- todo: include the recent initiatives -->
<!-- In this space, initiatives such as the Solid protocol, multiple Data Space initiatives such as
IDSA and PrometheusX and Digital Wallets provide the direction of the future of
decentralized data storage architectures for the Web. -->

<!-- 
To handle such sensitive data, decentralized data storage initiatives 
started to include control mechanisms into the network architecture.
[Possible mentions / citations: Solid protocol, International Data Space Association, Digital (Identity) Wallets, ...].
These network architectures enable the modeling and enforcement of access (and usage) requirements to automate trust flows in the network. -->


<!-- Provenance modeling?? -->

<!-- Combining the above - NEED -->

<!-- 
In these authorized data sharing networks, two main focal points are emerging.
Data sharing initiatives focus on providing protocols to enable data sharing
networks based on a connector architecture that existing data sources can 
connect to and register their data on. These connectors  manage a catalog that
supports any type of resource to be registered, and enforce both access
(and usage [FIND SOURCE!!]) requirements on top of the registered resources.
Such marketplaces require manual review for (agreement and?) integration of data.
On the other hand, initiatives such as Digital Identity Wallets focus on tight 
data models and standards to maximize integration of smaller sets of well managed
credentials in the network.  -->


<!-- WHAT ARE THE DOWNSIDES OF WALLETS??? -->

<!-- 
Where these wallets allow for strong integration,
they rely on strong centralized management of 
data models and authorization mechanisms, 
limiting their full potential.
[This is a pretty weak point, and they can adapt as well?? not sure] -->



<!-- [todo: look into access and usage control of these wallets more thoroughly]
[Local data storage, Wallets will be compliant with the General Data Protection Regulation and Cybersecurity certified.]
[At the mercy of data sharing capabilities set by centralized instances] -->

 <!--https://ec.europa.eu/digital-building-blocks/sites/display/EUDIGITALIDENTITYWALLET/Security+and+Privacy  -->

<!-- 
In these authorized data sharing ecosystems, we see the emergence of two ecosystem designs.
The data spaces initiatives focus on digital data markeplaces as emerging ecosystems that 
can steer innovation through interoperability of standards for exchanging data on the Web.
The focus here is on connecting existing infrastructures that handle data into such a 
sharing network through connector architectures and alignment on these connectors
in terms of how data can be added to their catalog and how policies can be enforced over the data. [Europe initiatives. IDSA. PrometheusX, ...]
On the other side there is a push for wallets and digital identifiers that combine the notion of 
protected data with the requirement that the data stored in these wallets must be widely integrated,
in the same notion that a passport can be used internationally and still is recognized as a valid identifier.
The focus here is not on the quantity or variety of data supported, but on the interoperability and
verifiability of smaller sets of data to enable maximal integration. -->







<!-- 
* 3 parts: interop and trust in data, in access control and usage control

* Second part of automation requires modeling the required flows of trust throughout these decentralized systems for data sharing
* Work on verifiable credentials
* Work on GDPR in ODRL  

* Raw Data Now <-> Trust Envelopes! 
* -->
