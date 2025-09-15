This project presents a scalable pipeline for the automatic discovery of hidden foreignkey/primary-key (FK–PK) relationships within legacy enterprise datasets. This
pipeline was developed in partnership with Vodafone as part of the Analytics Project.
Legacy databases frequently experience a loss of explicit meaningful relationships
over time, which can significantly complicate critical tasks such as data integration,
migration, and analytics. The proposed methodology utilizes a diverse approach,
using metadata extraction, heuristic candidate generation, multi-feature scoring, and
efficient composite-keys discovery. This integrated framework enables the inference
of implicit relationships, removing the need for prior documentation.
Firstly, column-level metadata is extracted, including name tokens, data types,
length distributions, uniqueness ratios, and null densities, from ten tables of the
ODS CAMA PRD schema. Subsequently, both single-column and composite candidates are generated, with domain-knowledge-driven and super-set pruning techniques
employed to manage combinatorial complexity. Each candidate is evaluated using a
weighted model that incorporates name similarity, data type compatibility, length
distribution, alignment, uniqueness metrics, and audit-field penalties. The most
qualified candidates are subjected to a final verification process using subset-matching
to ensure referential integrity.
Empirical evaluation on real Vodafone datasets shows that the pipeline reliably
recovers known FK–PK relationships and completes end-to-end on regular hardware
in well under an hour. The transparent scoring framework provides per-match
explanations and audit trails, which supports stakeholder trust and smooth integration
into Vodafone’s ETL workflows. Finally, we discuss practical recommendations for
embedding the solution within Vodafone’s data governance processes and future
extension for pipeline workflow.
