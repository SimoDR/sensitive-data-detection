# Sensitive data detection 

This repository contains the dataset used for sensitive data detection as described in the paper "Exploiting Large Language Models to Train Automatic Detectors of Sensitive Data" (currently submitted for review in the [IRCDL 2024 Conference]([url](http://ircdl2024.dei.unipd.it/))...). As described in the paper, the dataset has been generated with the OpenLLaMa model [[1]](#1), and as such is licensed permissively under the Apache 2.0 license: we decided to distribute it freely to encourage further research in this field.

## Format

The dataset is shaped as a list of entries: each top-level entry is a couple `(text, label)`, where:
- `text` holds the content of the generated document;
- `label` is a list of entries, in with the key is a label specifying the category of sensitive data, the value is a list of pairs, each pair indicating the beginning and ending character index of the sensitive span.

## Categories and labels

The labels used in the dataset follows with a brief description:
- **\[DATI_SALUTE\]**: This category encompasses information pertaining to the physical and mental well-being of individuals. It includes details regarding existing diagnoses, medical conditions, and disabilities.
- **\[DATI_POLITICA\]**: The political category involves information related to an individual's political beliefs. This encompasses their political orientation, specific party affiliation, as well as membership in work unions or similar organizations.
- **\[DATI_SESSUALITA\]**: Within the realm of sexuality, we consider information concerning an individual's sexual orientation, habits, and gender identity.
- **\[DATI_GIUDIZIARI\]**: The judicial category encompasses data associated with legal matters, such as offenses, crimes, charges, pending criminal proceedings, accusations, and trial proceedings involving an individual.
- **\[DATI_RELIGIONE\]**: Information regarding an individual's philosophical and religious beliefs and affiliations falls within the scope of the philosophy category.
- **\[DATI_ETNIA\]**: The ethnic category pertains to an individual's ethnic origin and heritage.

## Document types and count

| Data category              | Doc title                                           | Doc count | Avg char count |
|----------------------------|-----------------------------------------------------|-----------|----------------|
| **Mix (Sensitive)**         | Email                                               | 233       | 1072.91        |
|                            | Newspaper article                                   | 148       | 1004.84        |
|                            | Curriculum Vitae                                    | 109       | 1241.66        |
|                            | **TOT**                                             | **490**   |                |
| **Health & Sexuality**      | Psychiatric report                                  | 83        | 1638.61        |
|                            | Medical prescription                                | 71        | 1372.89        |
|                            | Medical records                                     | 62        | 1476.06        |
|                            | Psychological evaluation                            | 53        | 1899.11        |
|                            | Certification of invalidity                         | 20        | 1419.95        |
|                            | Biopsy results                                      | 21        | 1123.29        |
|                            | Eye test report                                     | 15        | 1455.33        |
|                            | Surgery report                                      | 15        | 1475.53        |
|                            | Blood tests                                         | 10        | 1437.5         |
|                            | Certificate of civil union                          | 20        | 1116.95        |
|                            | **TOT**                                             | **370**   |                |
| **Judicial**               | Denunciation report                                 | 26        | 1225.58        |
|                            | Police identikit                                    | 25        | 1097.16        |
|                            | Criminal record                                     | 24        | 1305.08        |
|                            | Arrest report                                       | 19        | 1234.16        |
|                            | Notice of investigation                             | 24        | 1806.88        |
|                            | Criminal judgement                                  | 22        | 1403.82        |
|                            | Notice of conclusion of preliminary investigations | 19        | 1610.89        |
|                            | Certificate of pending charges                      | 14        | 1268.14        |
|                            | Precautionary measures                              | 18        | 1281.28        |
|                            | **TOT**                                             | **191**   |                |
| **Politic**                | Political endorsement                               | 38        | 735.39         |
|                            | Union card                                          | 30        | 1066.77        |
|                            | Party card                                          | 28        | 1067.14        |
|                            | **TOT**                                             | **96**    |                |
| **Philosophical**          | Philosophical endorsement                           | 68        | 1028.49        |
|                            | Baptismal certificate                               | 32        | 783.47         |
|                            | Certificate of participation to religious group     | 32        | 682.59         |
|                            | **TOT**                                             | **132**   |                |
| **Ethnic**                 | DNA analysis report                                 | 37        | 1804.86        |
|                            | Ancestry analysis report                            | 31        | 1824.16        |
|                            | Birth certificate                                   | 36        | 435.61         |
|                            | Genealogical tree report                            | 30        | 1444.67        |
|                            | **TOT**                                             | **134**   |                |
| **Other (Non sensitive)**  | Scientific paper                                    | 106       | 3038.55        |
|                            | Advertising flyer for event                         | 92        | 992.42         |
|                            | Scientific publications report                      | 88        | 2576.69        |
|                            | Marriage certificate                                | 66        | 829.39         |
|                            | Advertising flyer                                   | 18        | 1035.83        |
|                            | Company invoice                                     | 17        | 1203.71        |
|                            | Services and products catalogue                     | 15        | 2122.2         |
|                            | Financial report by corporate                       | 14        | 2215.5         |
|                            | Commercial report                                   | 13        | 2128.92        |
|                            | City travel guide                                   | 12        | 1598.75        |
|                            | Tax declaration                                     | 12        | 1476.58        |
|                            | Cooking recipe                                      | 11        | 1168.64        |
|                            | Corporate memo                                      | 9         | 1277.67        |
|                            | Company balance sheet                               | 8         | 1443.12        |
|                            | Book review                                         | 7         | 767            |
|                            | Wikipedia extract                                   | 150       | 2430.3         |
|                            | **TOT**                                             | **638**   |                |

## References 

<a id="1">[1]</a>
Geng, Xinyang and Liu, Hao,
OpenLLaMA: An Open Reproduction of LLaMA,
https://github.com/openlm-research/open_llama
