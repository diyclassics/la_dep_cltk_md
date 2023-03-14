<!-- SPACY PROJECT: AUTO-GENERATED DOCS START (do not remove) -->

# 🪐 spaCy Project: la_dep_cltk_md

Code required to train spaCy-compatible md model for Latin. Latin pipeline with POS tagger, morphologizer, lemmatizer, and dependency parser trained on all available Latin UD treebanks, i.e. Perseus, PROIEL, ITTB,  UDante, and LLCT (see below). The model contains floret vectors trained on Wikipedia, Oscar, and UD data. Note also that a sm model (i.e. without vectors) is trained in the same pipeline.


## 📋 project.yml

The [`project.yml`](project.yml) defines the data assets required by the
project, as well as the available commands and workflows. For details, see the
[spaCy projects documentation](https://spacy.io/usage/projects).

### ⏯ Commands

The following commands are defined by the project. They
can be executed using [`spacy project run [name]`](https://spacy.io/api/cli#project-run).
Commands are only re-run if their inputs have changed.

| Command | Description |
| --- | --- |
| `assets` | Download assets |
| `preprocess` | Convert different UD treebanks so that they use shared formatting, feature defs, etc. |
| `convert` | Convert the data to spaCy's format |
| `norm-corpus` | Convert norm attribute to u-v and i-j norm |
| `extract-wikipedia` | Convert Wikipedia XML to JSONL with wikiextractor |
| `tokenize-wikipedia` | Tokenize and sentencize Wikipedia |
| `tokenize-oscar` | Tokenize and sentencize OSCAR dataset |
| `tokenize-ud` | Tokenize and sentencize UD; following wikipedia/oscar pattern |
| `create-input` | Concatenate tokenized input texts |
| `train-floret-vectors` | Train floret vectors |
| `load-vectors` | load floret vectors |
| `init-labels` | Initial labels for components |
| `train-sm` | Train sm tagger/parser on Latin UD treebanks |
| `train` | Train tagger/pagger on Latin UD treebanks |
| `evaluate-sm` | Evaluate on the test data and save the metrics |
| `evaluate` | Evaluate on the test data and save the metrics |
| `package-sm` | Package the trained sm model so it can be installed |
| `package` | Package the trained model so it can be installed |
| `document` | Document dep_cltk_md |
| `clean` | Remove intermediate files |

### ⏭ Workflows

The following workflows are defined by the project. They
can be executed using [`spacy project run [name]`](https://spacy.io/api/cli#project-run)
and will run the specified commands in order. Commands are only re-run if their
inputs have changed.

| Workflow | Steps |
| --- | --- |
| `all` | `assets` &rarr; `preprocess` &rarr; `convert` &rarr; `norm-corpus` &rarr; `extract-wikipedia` &rarr; `tokenize-wikipedia` &rarr; `tokenize-oscar` &rarr; `tokenize-ud` &rarr; `create-input` &rarr; `train-floret-vectors` &rarr; `load-vectors` &rarr; `init-labels` &rarr; `train-sm` &rarr; `train` &rarr; `evaluate-sm` &rarr; `evaluate` &rarr; `package-sm` &rarr; `package` &rarr; `document` &rarr; `clean` |

### 🗂 Assets

The following assets are defined by the project. They can
be fetched by running [`spacy project assets`](https://spacy.io/api/cli#project-assets)
in the project directory.

| File | Source | Description |
| --- | --- | --- |
| `assets/original/UD_Latin-Perseus` | Git |  |
| `assets/original/UD_Latin-PROIEL` | Git |  |
| `assets/original/UD_Latin-ITTB` | Git |  |
| `assets/original/UD_Latin-LLCT` | Git |  |
| `assets/original/UD_Latin-UDante` | Git |  |
| `vectors/downloaded/wikipedia/lawiki-latest-pages-articles.xml.bz2` | URL |  |

<!-- SPACY PROJECT: AUTO-GENERATED DOCS END (do not remove) -->

## Install

- To install the current version...
    - `pip install https://huggingface.co/diyclassics/la_dep_cltk_md/resolve/main/la_dep_cltk_md-0.3.1/dist/la_dep_cltk_md-0.3.1.tar.gz`

## Model repository

- The model itself can be found here:
    - https://huggingface.co/diyclassics/la_dep_cltk_md

## Current version

| Feature | Description |
| --- | --- |
| **Name** | `la_dep_cltk_md` |
| **Version** | `0.3.1` |
| **spaCy** | `>=3.5.1,<3.6.0` |
| **Default Pipeline** | `normer`, `tok2vec`, `tagger`, `morphologizer`, `trainable_lemmatizer`, `parser` |
| **Components** | `senter`, `normer`, `tok2vec`, `tagger`, `morphologizer`, `trainable_lemmatizer`, `parser` |
| **Vectors** | -1 keys, 50000 unique vectors (300 dimensions) |
| **Sources** | UD_Latin-Perseus<br />UD_Latin-PROIEL<br />UD_Latin-ITTB<br />UD_Latin-LLCT<br />UD_Latin-UDante |
| **License** | `MIT` |
| **Author** | [Patrick J. Burns; with Tim Geelhaar](https://diyclassics.github.io/) |

### Accuracy

| Type | Score |
| --- | --- |
| `SENTS_F` | 85.24 |
| `SENTS_P` | 85.84 |
| `SENTS_R` | 84.65 |
| `TAG_ACC` | 92.92 |
| `POS_ACC` | 96.50 |
| `MORPH_ACC` | 91.86 |
| `LEMMA_ACC` | 94.17 |
| `DEP_UAS` | 81.75 |
| `DEP_LAS` | 74.51 |
| `TOK2VEC_LOSS` | 10216731.34 |
| `TAGGER_LOSS` | 1009750.56 |
| `MORPHOLOGIZER_LOSS` | 2018163.87 |
| `TRAINABLE_LEMMATIZER_LOSS` | 746248.75 |
| `PARSER_LOSS` | 6078691.87 |

NB: For full details on tags etc., see the README.md in the model package.
