# onto-hcv
Onto-HCV: an OWL ontology for human-centric vulnerabilities in cognitive cities
Add files via upload
# Onto-HCV

**Onto-HCV: an Ontology for Human-Centric Vulnerabilities in Cognitive City Systems**

Ontology IRI: `https://w3id.org/ontohcv`
Current version: **v18.2** (November 2026)

## Purpose

Onto-HCV is a formal model that infers human-centric vulnerabilities in smart and
cognitive city systems from a written description of the system. Each vulnerability
is represented as a condition over system elements, actors, data flows and controls,
so that the reasoner identifies a vulnerability where the described state of the
system enables it. Each identified vulnerability is mapped to security (STRIDE) and
privacy (LINDDUN) threat categories. The vulnerability set is taken from a published
multidimensional taxonomy of human-related vulnerabilities.

## Repository structure

```
ontology/
    OntoHCV_v18_2.ttl                            the ontology (TBox and rules)
    catalog-v001.xml                             import resolution for Protege
cases/
    OntoHCV_Case_Oldsmar_Reported_v18_2.ttl      test case 1 (ABox)
    OntoHCV_Case_NoiseApp_DPIA_v18_2.ttl         test case 2 (ABox)
results/
    OntoHCV_Oldsmar_v18_2_inferred.owl           reasoned model, test case 1
    OntoHCV_NoiseApp_v18_2_inferred.owl          reasoned model, test case 2
queries/
    competency-questions.md
```

Keep `catalog-v001.xml` in the same folder as the ontology file. It resolves both
`https://w3id.org/ontohcv` and `https://w3id.org/ontohcv/18.2` to
`OntoHCV_v18_2.ttl`, so the case files load without network access.
