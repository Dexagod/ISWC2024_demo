### Guiding use case
{:#use_case}

To contextualize the trust flows internal
to Web platforms and their translation
into the network architecture for 
decentralized data stores, 
a guiding use case and its 
requirements are presented. 
<!-- use case -->
The use case is as follows:
Services in the network need to automate 
the integration of user age to provide
users with age restricted functionality.
<!-- Platforms -->
In the case of Web platforms,
such data integrations are automated
on top of internal trust flows 
in the platform.
1. Integrated services trust the platform to provide an age that has been verified externally if this is indicated in the data model.
2. Users trust platforms to model and enforce governance requirements according to platform policy, user preferences as defined in their data sharing settings, as well as any legal requirements.
3. Integrated services trust their processing of the data to comply to these requirements when integrating data from the platform.
<!-- Our use case -->
To translate these requirements to a network
architecture for decentralized data stores,
these trust flows must be translated into
the following requirements to enable
automated integration of data:
1. Services in the network must be able to discover age related data carrying sufficient proof of data integrity.
2. Users must trust their data stores to be able to model and enforce their preferences and any relevant legal requirements depending on the type of data usage.
3. Services in the network trust that a successful data exchange enables them to use the retrieved data as defined by the conditions defined in the exchange.

 <!-- todo: Needs a final rewrite to make it clean  -->