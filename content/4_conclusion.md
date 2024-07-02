## Conclusion
{:#conclusion}

With this work, we show that we can build a 
minimal network architecture for modeling 
trust flows in a network of decentralized
data stores.
(i) Combining the Linked Data Platform specification
with the Verifiable Credentials specification provides
the capabilities for storage and retrieval of credentials
issued in the network. In combination with a simple index,
this provides sufficient capabilities for automating
integration of data with sufficient trust in integrity.
(ii) The combination the UMA protocol, with the modeling
and evaluating of policies using the ODRL and DPV policy
ontologies provide the required expressivity to both
model and evaluate both user and legal requirements. [CITE AGAIN!!!]
The capability for modeling, negotiating and evaluating
these requirements forms the basis for automating the 
authorization process for data integration.
<!-- Should UMA separation be mentioned here? -->
(iii) Through an instantiation mechanism, 
the requirements for access and usage of 
the data are established in an instantiated
policy.
This instantiated policy forms the agreement
under which the data exchange has taken place
and can be used to prove the use or misuse 
of data under these conditions.
Auditing systems can make use of such machine
readable agreements to automate verification
of the agreements and the checking of the conditions.


Future work on this is planned to include the following considerations.
For data integration (i) we aim to focus selective disclosure credentials
that can be auto generated based on a data request. [todo: similar to EU wallets!]
For governance (ii) the inclusion of usage requirements
in the negotiation combined with the modeling of access
control requirements in the form of verifiable credentials
continues data integrity in the policy evaluation mechanism.
Finally, policy instantiation (iii) requires additional work
to formalize the generation of such instantiations.