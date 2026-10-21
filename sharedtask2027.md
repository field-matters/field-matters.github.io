---
title: Field Matters 2027 – Shared Task
description: Field Matters 2027 Shared Task on Automatic Interlinear Glossing.
image: https://field-matters.github.io/logo.jpg
---
  
# Field Matters 2027 Shared Task on Automatic Interlinear Glossing

## Important links
- [Announcements and general contact (Google group)](https://groups.google.com/g/fm-shared-task-glossing-2027)
- GitHub repository (TBA)
- Registration (Google form) (TBA)
- CodaBench competition (TBA)

## Important dates
- Shared Task details finalised: 26/10/2026
- Phase 1: Beginning of the development phase: 26/10/2026
- Phase 2: Information about the new languages: 03/11/2026
- Phase 3: Test set release (beginning of the test phase): mid/end of November
- Output submission deadline: end of November/beginning of December
- System description deadline: December 15, 2026
- Notification of acceptance: January 11, 2027
- Camera-ready deadline: January 22, 2027
- Workshop dates: March 9-14, 2027

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
In our Shared Task, the input is mainly the **unsegmented source sentence** (first row). Some instances will be accompanied by its translation in a high-resource language (usually, in English; fourth row).

## Timeline

The Shared Task will be in **three phases**:
- Phase 1: The development phase starts with the 6 languages mentioned below.
- Phase 2: The development phase continues with information about new languages ('surprise languages').
- Phase 3: The test phase starts with the release of the test sets.



## Dataset

In phase 1, the datasets to consider will be the training and dev sets. Although the test sets for this set of languages are publicly available, they should **NOT** be used to train the system.  
The goal of this set is to have a common ground between submitted systems and previous work.

In phase 2, we will mainly release new **test** datasets due to licensing restrictions. There will be no training data.


#### Training data restrictions
Regarding training data for glossing, we restrict the glossing data to those released in the GitHub repository + the publicly accessible multilingual IGT datasets GlossLM and PolyGloss:
- [GlossLM](https://huggingface.co/datasets/lecslab/glosslm-corpus)
- [PolyGloss](https://huggingface.co/datasets/lecslab/polygloss-corpus)

If you wish to use other *glossed* corpora, please let us know beforehand to check for dataset overlap.  
Regarding **non-glossed** data (e.g., unlabelled data, sentences with another type of label, dictionaries, grammar books (without overlapping examples)), any publicly available dataset is allowed.  


## Evaluation

We will mainly evaluate the quality of the predicted gloss. However, we encourage submissions to be able to handle *morphological segmentation* (second tier of Figure 1), since field linguists usually analyse sentences into morphemes before producing glosses.

We will use the following metrics to evaluate the predicted gloss quality: *Morpheme Error Rate* (MER), *Word-level Accuracy*, and *Morpheme-level Accuracy*.  
The main metric for the ranking is **MER**, following [Ginn et al., (2026)](https://aclanthology.org/2026.acl-long.1657/), while both accuracy scores follow the previous literature for information purposes.



## Submission
TBA



## Citations
### Evaluation datasets

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