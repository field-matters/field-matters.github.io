---
title: Field Matters 2027 – Shared Task
description: Field Matters 2027 Shared Task on Automatic Interlinear Glossing.
image: https://field-matters.github.io/logo.jpg
---
  
# Field Matters 2027 Shared Task on Automatic Interlinear Glossing

## Important links
- [Announcements and general contact (Google group)](https://groups.google.com/g/fm-shared-task-glossing-2027)
- [GitHub repository](https://github.com/field-matters/ST2027)
- [Registration (Google form)](https://forms.gle/v8wYmSyyLHptSfov9)
- CodaBench competition (TBA)

## Important dates (DD/MM/YYYY)
- Shared Task details finalised: 26/10/2026
- Phase 1: Beginning of the development phase: 26/10/2026
- Phase 2: Information about the new languages: 03/11/2026
- Phase 3: Test set release (beginning of the test phase): 16/11/2026
- Output submission deadline: 08/12/2026
- System description deadline: 15/12/2026
- Notification of acceptance: 11/01/2027
- Camera-ready deadline: 22/01/2027
- Workshop dates: 14/03/2027

**All deadlines are 23:59 UTC-12 ('Anywhere on Earth').**

## Description

This year, we offer a shared task on automatic interlinear glossing for field linguistic annotations.

<table>
  <tr>
    <th>source sentence</th>
    <td>Zbz</td>
    <td>sc</td>
    <td>tqwaipele</td>
    <td>tqnginipenge</td>
    <td>kraesz'mz</td>
  </tr>
  <tr>
    <th>morphological segmentation</th>
    <td>zbz</td>
    <td>sc</td>
    <td>tq-wai-pe-le</td>
    <td>tq-ngini-pe-nge</td>
    <td>kraesz'mz</td>
  </tr>
  <tr>
    <th>interlinear gloss</th>
    <td>so.then</td>
    <td>PFV</td>
    <td>RL-do-COS-3MINIA</td>
    <td>RL-become-COS-1MINII</td>
    <td>sixth</td>
  </tr>
  <tr>
    <th>translation</th>
    <td colspan="5"><i>So then that's how I became the sixth.</i></td>
  </tr>
</table>

Figure 1: An Interlinear Glossed Text (IGT) for a sentence in Natugu.


The task is to predict interlinear glosses, which are morpheme-level linguistic annotations, as shown in the third row of the figure above, notably used in field linguistics. 
Ultimately, such glossing systems aim to help field linguists with the annotation task for languages under documentation, as it is mainly performed manually with little automation. 

This Shared Task follows the [SIGMORPHON 2023 Shared Task on Interlinear Glossing](https://github.com/sigmorphon/2023GlossingST).  
In our Shared Task, the input is mainly the **unsegmented source sentence** (first row). Some instances will be accompanied by their translation in a high-resource language (usually, in English; fourth row).
The goal is to predict the **glossed sentence** (third row).

## Timeline

The Shared Task will be in **three phases**:
- Phase 1: The development phase starts with the 5 languages mentioned below.
- Phase 2: The development phase continues with information about new languages ('surprise languages').
- Phase 3: The test phase starts with the release of the test sets.

## Languages

The task will cover the following languages:
- [Phase 1] 4 from the previous SIGMORPHON 2023 Shared Task on Interlinear Glossing: Gitksan (git), Lezgi (lez), Natugu (ntu), and Nyangbo (nyb).
- [Phase 1] 1 language from the [Glossed Audio Corpus of Ainu Folklore](https://ainu.ninjal.ac.jp/folklore/en/) via the [Fieldwork corpus](https://huggingface.co/datasets/wav2gloss/NINJAL-Ainu-Folklore) ([He et al., 2024](https://aclanthology.org/2024.acl-long.34/)): Hokkaido Ainu (ain).
- [Phase 2] **5 new languages** with mostly test data (sorted alphabetically):
  - Amis (`ami`, `amis1246`): Austronesian (Formosan) language spoken in Taiwan
  - Even (`eve`, `ewen1234`): Tungusic language spoken in Siberia
  - Japhug (`jya`, `japh1234`): Sino-Tibetan (Gyalrong) language spoken in Southwestern China
  - Mukri Kurdish (`ckb`, `mukr1239`): Indo-European (Indo-Iranian) language spoken in the northwestern part of Iran; it belongs to the dialect group of Central Kurdish (`ckb`).
  - Tsou (`tsu`, `tsou1248`): Austronesian language spoken in Taiwan.

The corresponding citations for the languages are detailed in a section below.

## Submission rules

Submissions to the shared task should follow the rules below:
- Model: Any type of model is allowed, provided that the system is based on *open-source* or *open-weight* models (if LLM-based).   
We encourage you to upload your system to GitHub or HuggingFace.  
Closed-source models can be used for other purposes (e.g., summarising a grammar book, generating pseudo-training data)
- Dataset: Regarding the glossing dataset, we consider the GlossLM/PolyGloss dataset as the main *labelled* dataset to use.  
More details on the allowed datasets are below.
- Participation tracks: We consider two sets of languages: 
  - `existing_set` (from phase 1; SIGMORPHON languages + Ainu) and 
  - `new_set` (from phase 2; new languages). 

Participation can be in only one of the two sets, or in both. However, in any case, a submission should contain predictions for all languages of a set (5 languages for `existing_set` and 5 languages for `new_set`).  
Since the test sets of the `existing_set` are available online, we kindly ask participants **not** to use them for training.

In case of doubt about a rule, please feel free to check with us.

## Dataset

In phase 1, the datasets to consider will be the training and dev sets. Although the test sets for this set of languages are publicly available, they should **NOT** be used to train the system.  
The goal of this set is to have a common ground between submitted systems and previous work.

In phase 2, we will mainly release new **test** datasets due to licensing restrictions.  
To help calibrate the models, we provide at least **two fully segmented and glossed sentences** in our [GitHub repository](https://github.com/field-matters/ST2027).


#### Training data restrictions
Regarding training data for glossing, we restrict the glossing data to those released in the GitHub repository + the publicly accessible multilingual IGT datasets GlossLM and PolyGloss:
- [GlossLM](https://huggingface.co/datasets/lecslab/glosslm-corpus)
- [PolyGloss](https://huggingface.co/datasets/lecslab/polygloss-corpus)

If you wish to use other *glossed* corpora, please let us know beforehand to check for dataset overlap.  
Regarding **non-glossed** data (e.g., unlabelled data, sentences with another type of label, dictionaries, grammar books (without overlapping examples)), any publicly available dataset is allowed.  


## Evaluation

We will mainly evaluate the quality of the predicted gloss. However, we encourage submissions to be able to handle *morphological segmentation* (second tier of Figure 1), since field linguists usually analyse sentences into morphemes before producing glosses.

We will use the following metrics to evaluate the predicted gloss quality: *Morpheme Error Rate* (MER), *Word-level Accuracy*, and *Morpheme-level Accuracy*.  
The main metric for ranking is **MER**, following [Ginn et al. (2026)](https://aclanthology.org/2026.acl-long.1657/), while both accuracy scores follow the previous literature for information purposes.

We will average each language's evaluation metric scores per language set.

## Output submission
Submission format and method TBA very soon.

Several submissions can be made, but only **one main submission** (to be decided by the participants before the result announcement) will be considered. The main submission is to be specified **per track**; it can a different system *per track* (but *not inside a track*).

The deadline for the submission is: **08/12/2026** (AoE).

## System description
Participation in the Shared Task is valid **only** when a system description article is written about the output submission. We acknowledge that the timeline for the Shared Task is quite tight: we therefore recommend that each participant start writing it as soon as possible.  
Please let us know if you require any deadline extension or any support regarding the writing (e.g., mentorship).  

System descriptions mostly follow the general policy as for our workshop submissions (i.e., the standard \*ACL submissions). Articles should use the same \*ACL template. However, there are two differences:
- Page length: system description articles should have a maximum of **6 pages** (excluding Limitations, Ethical considerations, References, and Appendices) for the submission (there will be an extra page for the camera-ready version)
- Anonymity: the submissions should not be anonymised. It should be clear to the reviewer which submission is described (e.g., a title with the team name).

The system description should be clear about the following points:
- the participation track(s)
- the dataset(s) that were used for training and development (including example selection, if there is retrieval)
- the licence of any *external* datasets
- the model(s) which were used
- the overall methodology of the system
- the systems leading to the submitted outputs for the shared task, with an emphasis on **one main submission**.

System descriptions for the Shared Task should also be submitted on the main OpenReview submission platform (cf. workshop guidelines). Accepted system descriptions will also be in the workshop proceedings.  
The deadline for the system description article is: **15/12/2026** (AoE).

The citation for our Findings article regarding the Shared Task will be given soon.



## Citations
### Evaluation datasets
#### SIGMORPHON 2023 Shared Task
To acknowledge the SIGMORPHON 2023 Shared Task, please cite the following article:
- Michael Ginn, Sarah Moeller, Alexis Palmer, Anna Stacey, Garrett Nicolai, Mans Hulden, and Miikka Silfverberg. 2023. [Findings of the SIGMORPHON 2023 Shared Task on Interlinear Glossing](https://aclanthology.org/2023.sigmorphon-1.20/). In *Proceedings of the 20th SIGMORPHON workshop on Computational Research in Phonetics, Phonology, and Morphology*, pages 186–201, Toronto, Canada. Association for Computational Linguistics.

#### Hokkaido Ainu
- The Glossed Audio Corpus of Ainu Folklore corpus.  
Hiroshi Nakagawa; Anna Bugaeva; Miki Kobayashi and Yoshimi Yoshikawa (2016-2024) [A Glossed Audio Corpus of Ainu Folklore](https://ainu.ninjal.ac.jp/folklore/). NINJAL. 

#### New datasets
- TBA

### Potential training corpora
Here are the two versions of the multilingual glossed corpora, which can be used for training and which also contain some evaluation languages.
- The (first) GlossLM corpus.  
Michael Ginn, Lindia Tjuatja, Taiqi He, Enora Rice, Graham Neubig, Alexis Palmer, and Lori Levin. 2024. [GlossLM: A Massively Multilingual Corpus and Pretrained Model for Interlinear Glossed Text](https://aclanthology.org/2024.emnlp-main.683/). In *Proceedings of the 2024 Conference on Empirical Methods in Natural Language Processing*, pages 12267–12286, Miami, Florida, USA. Association for Computational Linguistics.
- The (second) PolyGloss corpus.  
Michael Ginn, Lindia Tjuatja, Enora Rice, Ali Marashian, Maria Valentini, Jasmine Xu, Graham Neubig, and Alexis Palmer. 2026. [Massively Multilingual Joint Segmentation and Glossing](https://aclanthology.org/2026.acl-long.1657/). In *Proceedings of the 64th Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers)*, pages 35806–35820, San Diego, California, United States. Association for Computational Linguistics.


## Acknowledgements

We warmly thank the organisers of the SIGMORPHON 2023 Shared Task, especially Michael Ginn, for their help.  

## Organisers
- Coordination: Field Matters organisers
- Dataset contribution: TBA

## Contact
We suggest using the [Google group](https://groups.google.com/g/fm-shared-task-glossing-2027) for general questions that may interest all participants.  
For private questions, please write to Shu Okabe (shu dot okabe at tum dot de).
