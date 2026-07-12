\# AS-005 Causal Relationship Standard



Version: 1.0



Status: Active



Owner: Project Atlas



Created: 2026-07-11



\---



\# 1. Purpose



This Standard exists to define how Atlas represents causal relationships between market entities and events.



Atlas does not merely record events.



Atlas explains why events happen and how they influence the capital market.



\---



\# 2. Core Principle



Every important event should be connected to its causes and consequences.



Knowledge is not a collection of isolated facts.



Knowledge is a network of relationships.



\---



\# 3. Causal Relationship Types



Atlas currently supports the following relationship types.



\---



\## Causes



Definition



Entity A directly causes Entity B.



Example



Interest Rate Cut



↓



Causes



↓



Lower Financing Costs



\---



\## Influences



Definition



Entity A has an influence on Entity B but is not the sole cause.



Example



Oil Price Increase



↓



Influences



↓



Airline Industry



\---



\## Supports



Definition



Entity A provides evidence or support for Entity B.



Example



Quarterly Report



↓



Supports



↓



Profit Growth Conclusion



\---



\## Contradicts



Definition



Entity A conflicts with Entity B.



Example



Company Statement



↓



Contradicts



↓



Market Rumor



\---



\## Belongs To



Definition



Entity belongs to another entity.



Example



CATL



↓



Belongs To



↓



Power Battery Industry



\---



\## Depends On



Definition



Entity B depends on Entity A.



Example



Lithium Battery Production



↓



Depends On



↓



Lithium Carbonate Supply



\---



\## Similar To



Definition



Historical relationship used for comparison.



Example



2026 NEV Policy



↓



Similar To



↓



2023 Purchase Tax Extension



\---



\# 4. Relationship Rules



Every relationship shall include:



• Source Entity



• Target Entity



• Relationship Type



• Evidence



• Confidence



• Created Time



• Updated Time



\---



\# 5. Evidence Requirement



Every causal relationship must be supported by evidence.



Acceptable evidence includes:



• Official announcements



• Company disclosures



• Government policies



• Financial reports



• Industry reports



Relationships without evidence SHALL NOT enter Atlas.



\---



\# 6. Reasoning Chain



Atlas AI shall always explain conclusions using a reasoning chain.



Example



Government Policy



↓



Industry Growth



↓



Company Revenue



↓



Profit Expectation



↓



Market Valuation



↓



Stock Performance



The reasoning path must remain transparent and traceable.



\---



\# 7. Compliance



Relationships violating this Standard shall be rejected.



\---



\# AI Enforcement



Before creating a relationship, the AI must verify:



□ Source Entity exists



□ Target Entity exists



□ Relationship Type is valid



□ Evidence is available



□ Confidence level assigned



□ Timeline recorded



Only after all checks pass may the relationship enter the Atlas Knowledge Graph.

