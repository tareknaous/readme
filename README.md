# ReadMe++: Multilingual Multi-domain Benchmark for Sentence Readability Assessment

ReadMe++ is a multilingual multi-domain dataset with human annotations of 9757 sentences in Arabic, English, French, Hindi, and Russian collected from 112 different data sources.

The dataset is annotated for readability according to the CEFR framework (1-6 scale) and is openly-accessible for personal, research, and non-commercial purposes.

We also release a python package of ReadMe++ to easily use our fine-tuned language models for readability prediction, see simple usage steps below!

## Installation

```python
pip install readmepp
```

## Usage

First import the class ```ReadMe``` and create a BERT predictor instance of it.\
The parameter ```lang``` is to specify language (we support "en", "ar", "fr", "ru", and "hi").

```python
from readmepp import ReadMe

predictor = ReadMe(lang='en')
```

To assess the readability of a sentence, use the ```predict``` function of the model:

```python
sentence = 'Eukaryotes differ from prokaryotes in multiple ways, with unique biochemical pathways such as sterane synthesis.'

prediction = predictor.predict(sentence)

print(f"Predicted Readability Level: {prediction}")
```

Output:
```
Predicted Readability Level: 5
```


## Citation
For more details, see the accompanying paper: ["ReadMe++: Benchmarking Multilingual Language Models for Multi-Domain Readability Assessment"](https://arxiv.org/abs/2305.14463), **arxiv pre-print**, and please use the citation below.

```
@article{naous2023readme,
  title={ReadMe++: Benchmarking Multilingual Language Models for Multi-Domain Readability Assessment},
  author={Naous, Tarek and Ryan, Michael J and Lavrouk, Anton and Chandra, Mohit and Xu, Wei},
  journal={arXiv preprint arXiv:2305.14463},
  year={2023}
}
```

## Additional Access
**Medical Clinical Reports**: To access the sentences and labels of Clinical Reports (en), please [obtain permission](https://www.i2b2.org/NLP/DataSets/) from its original authors then email tareknaous@gatech.edu

**Hindi Product Review**: To access the sentences and labels of Hindi Product Review (hi), please [obtain permission](https://docs.google.com/forms/d/e/1FAIpQLSekp8FJzlPIKBghMSuyewOb5ZmBFmWrsLz3V_qcLqUxsCOGfg/viewform) from its original authors then email tareknaous@gatech.edu

## Contact
**Tarek Naous**: [Scholar](https://scholar.google.com/citations?user=ImyLv44AAAAJ&hl=en) | [Github](https://github.com/tareknaous?tab=repositories) |
[Linkedin](https://www.linkedin.com/in/tareknaous/) |  [Research Gate](https://www.researchgate.net/profile/Tarek_Naous?ev=hdr_xprf) | [Personal Wesbite](https://www.sites.google.com/view/tareknaous)
| tareknaous@gatech.edu

## Dependencies
The following are the versions of libraries used when the readme python package was developed:
More recent versions would also work.

```
transformers 4.35.2
torch 2.1.0+cu121
```
