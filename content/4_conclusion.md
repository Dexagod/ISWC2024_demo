## Conclusion
{:#conclusion}

With this demo, we show a minimal working 
architecture based on open Web specifications
that enable the modeling of these required 
trust flows in a network of decentralized
data stores:
(i) Combining the LDP storage model with
the use of VCs to represent data and context
provides the capabilities for storage and
trusted data integration in the network. 
<!-- this automated integration and trust in authenticity -->
(ii) The use of UMA to separate decouple
systems in the network enables the modeling
of user and legal requirements using ODRL and DPV,
and the ability to negotiate these requirements.
<!-- this automates trust in enforcing requirements -->
(iii) Instantiation the relevant access and usage 
requirements of a data exchange into a specific 
policy modeled using ODRL and DPV assigns responsibility.
Through the storage of these policies, 
the data provider can withdraw consent 
for specific data exchanges, 
while the receiving party can prove
their compliance to the usage requirements,
and auditing systems can automate certain 
verifications on top of these policies.

Future iteration on this architecture is planned to include the following considerations:
(i) Minimizing data requirements through selective disclosure
and expanding the scope of its associated metadata beyond integrity.
(ii) Formalizing requirement modeling and negotiations
to include data context requirements such as integrity
and usage requirements such as processing needs.
(iii) Formalizing a policy instantiation mechanism for ODRL and DPV.