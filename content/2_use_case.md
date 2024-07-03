### Guiding use case
{:#use_case}

To contextualize this translation
effort, a guiding use case and its 
requirements on the trust flows are
presented: 
<!-- use case -->
A service integrating with the network
of decentralized data stores must be able
to automate the integration of age to
enable restricted functionality.

<!-- Platforms -->
For a Web platform, an integrating 
service can make use of the following
internal trust flows between the
service, registered users and the
platform to automate integration:
(i) 
The service trusts the platform
to have verified the user age
when storing it internally as
a verified age.
(ii) 
The user trusts the platform to 
enforce governance requirements
according to their preference 
settings and legal requirements.
(iii) 
The service trusts that their
processing of platform data
complies with legal regulation
and user preference when retrieving
data over the internal APIs.
<!-- Our use case -->

To translate the above trust flows 
to a decentralized network of data stores, 
we present the following trust requirements
as necessary for services, data stores and 
users to automate the integration of age data:
(i) 
The service can discover user age data 
carrying sufficient and verifiable
proof of data integrity.
(ii) 
The user trusts their data store(s)
to model and enforce their preferences
and relevant legal requirements 
depending on the context of an interaction.
(iii) 
The service can trust a successful retrieval
of data to provide sufficient information
on how this data can be stored and used
in compliance with user preference
and legal regulation.

Note that the assumption is made that the
relevant policies and data are present.

 <!-- todo: Needs a final rewrite to make it clean  -->