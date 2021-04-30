# English - Vietnamese, French - Vietnamese bilingual corpus for Neural Machine Translation
The data is collected from TED talks. More detailed information about the data, please go to https://github.com/ngovinhtn/LowresMT/Datasets

## Datasets 

### 1. English-Vietnamese  
| Dataset       | Sentences | 
| ------------- | --------- | 
| Training Data | 231004 |
| Development (tst2012)  | 1553 |
| Test (tst2013)        | 1268 |


### 2. French-Vietnamese 
| Dataset       | Sentences | 
| ------------- | --------- | 
| Training Data | 203351 |
| Development   | 1007 |
| Test          | 1038 |


## Performance 
The results of our MT systems are measured in BLEU. We evaluate the best model for the baseline systems and the average scores on the five best models for the multilingual and pseudo systems. More details, please see our paper https://www.aclweb.org/anthology/2020.loresmt-1.8.pdf

### 1. English to Vietnamese 
| Models     | dev | tst |
| -----------| -----| ----------------- |
| Bilingual Baseline|  31.74 | 35.13 |
| Multilingual  | 31.66 (-0.08) |  36.18 (+1.05) |
| Multilingual + fine-tuning |31.88 (+0.14)| 36.56 (+1.43)|
|Multilingual + fine-tuning with similarity | 31.93 (+0.19) | 36.75 (+1.62)|
|Multilingual + fine-tuning with updated embedding | **32.11 (+0.37)**| **36.74 (+1.61)**|
|Multilingual + mixing pseudo bilingual data | 30.86 (-0.88) |  35.09 (-0.04)|

### 2. French to Vietnamese 

| Models     | dev | tst |
| -----------| -----| ----------------- |
| Bilingual Baseline|  23.07  | 23.03 |
| Multilingual  | 24.49 (+1.42) | 24.22 (+1.19)  |
| Multilingual + fine-tuning |24.51 (+1.44)  | 24.86 (+1.83)|
|Multilingual + fine-tuning with similarity | 24.37 (+1.30) | 24.70 (+1.63)|
|Multilingual + fine-tuning with updated embedding | 24.60 (+1.53)  | 24.96 (+1.93)|
|Multilingual + mixing pseudo bilingual data | **25.59 (+2.52)** | **25.57 (+2.54)**|
|Pseudo bilingual data translation | 19.00 | 18.71 |


## Citation
If you use these datasets, please cite our paper:
Thi-Vinh Ngo, Phuong-Thai Nguyen,Thanh-Le Ha, Khac-Quy Dinh, Le-Minh Nguyen: [Improving Multilingual Neural Machine Translation For Low-Resource
Languages: French, English - Vietnamese](https://www.aclweb.org/anthology/2020.loresmt-1.8.pdf). Proceedings of the 3rd Workshop on Technologies for MT of Low Resource Languages, pages 55–61, Decmber 04, 2020, (LowresMT 2020), Association for Computational Linguistics.

Bibtex:
```
@inproceedings{ngo-etal-2020-improving,
    title = "Improving Multilingual Neural Machine Translation For Low-Resource Languages: {F}rench, {E}nglish - {V}ietnamese",
    author = "Ngo, Thi-Vinh  and
      Nguyen, Phuong-Thai  and
      Ha, Thanh-Le  and
      Dinh, Khac-Quy  and
      Nguyen, Le-Minh",
    booktitle = "Proceedings of the 3rd Workshop on Technologies for MT of Low Resource Languages",
    month = dec,
    year = "2020",
    address = "Suzhou, China",
    publisher = "Association for Computational Linguistics",
    url = "https://www.aclweb.org/anthology/2020.loresmt-1.8",
    pages = "55--61",
}
```
