# Sensitive data detection 

This repository contains the dataset used for sensitive data detection as described in name_paper. It has been generated with the OpenLLaMa model, and as such is licensed permissively under the Apache 2.0 license.

## Format

The dataset is shaped as a list of entries: each top-level entry is a couple `(text, label)`, where:
- `text` holds the content of the generated document;
- `label` is a list of entries, in with the key is a label specifying the category of sensitive data, the value is a list of pairs, each pair indicating the beginning and ending character index of the sensitive span.

