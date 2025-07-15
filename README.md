# Agroecology tabular data schema: minimal example

This repository provides a **minimal example** of a dataset schema for an hypothetical dataset, structured using the [Frictionless Data Table Schema](https://specs.frictionlessdata.io/table-schema/) specification, for its use in the [Agroecology partnership](https://www.agroecologypartnership.eu/). The dataset is at `example.csv` and contains three fields: `crop_species`, `crop_yield_kg_per_ha` and `planting_date`.

The **schema** is represented in **multiple formats**:

- `example.schema.json` – official JSON Table Schema
- `example.schema.yaml` – same schema in YAML
- `example.schema.md` – Markdown version (not part of Frictionless)
- `example.schema.docx` – Word document version (not part of Frictionless)

While Markdown and Word are not accepted formats for machine-readable Frictionless Table Schemas, they are valuable as an entry point to encourage non-technical stakeholders to document their data. We consider that it's better to have documentation in a human-readable format than none at all. Converting a bullet point list in Markdown or Word to JSON/YAML later is a minimal effort compared to the cost of having undocumented data.

## Schema

This minimal example includes common Frictionless properties:

- `name`: field name in the dataset
- `type`: expected data type (e.g. string, number, date)
- `description`: human-readable explanation of the field
- `format`: expected format for values (e.g. date format)
- `rdfType`: semantic identifier for the concept the field represents

The property `rdfType` is an optional property we use to link each field to a **concept in a controlled vocabulary** or ontology. It helps machines (and humans) understand the meaning of a field beyond its name and link to many other resources in the web, and plays an important role in building AI-ready, machine-readable datasets and knowledge graphs.

For example, the [AGROVOC multilingual thesaurus by FAO](https://agrovoc.fao.org/) has a controlled vocabulary for the word "crop yield", linked to the same term in many languages and linkes to other concepts. It can be found at the URI below:
```yaml
http://aims.fao.org/aos/agrovoc/c_10176
```

Other ontologies with controlled vocabularies that are useful in Agroecology are the [Ecoportal](https://ecoportal.lifewatch.eu/), the [Agroportal](https://agroportal.lirmm.fr/) or the [Survey Ontology](https://cefriel.github.io/survey-ontology/docs/index.html).
