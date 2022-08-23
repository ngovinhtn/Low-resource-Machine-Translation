# English - Vietnamese, French - Vietnamese, Chinese - Vietnamese and Japanese - Vietnamese bilingual corpus for Neural Machine Translation
The data is collected from TED talks. More detailed information about the data, please go to https://github.com/ngovinhtn/LowresMT/Datasets
**License and copyright notices**: These datasets are followed policies of TED Talks (at https://www.ted.com/). They are **only used for research purposes and non-commercial**.

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

### 3. Chinese - Vietnamese 
| Dataset       | Sentences | 
| ------------- | --------- | 
| Training Data | 244076 |
| Development   | 1316 |
| Test          | 1296 |

### 4. Japanese - Vietnamese 
| Dataset       | Sentences | 
| ------------- | --------- | 
| Training Data | 244117 |
| Development   | 568 |
| Test          | 1220 |

## Performance 
The results of our MT systems are measured in BLEU. We evaluate the best model for the baseline systems and the average scores on the five best models for the multilingual and pseudo systems. More details, please see our paper https://www.aclweb.org/anthology/2020.loresmt-1.8.pdf

### 1. English to Vietnamese (Ngo et al. 2020)
| Models     | dev | tst |
| -----------| -----| ----------------- |
| Bilingual Baseline|  31.74 | 35.13 |
| Multilingual  | 31.66 (-0.08) |  36.18 (+1.05) |
| Multilingual + fine-tuning |31.88 (+0.14)| 36.56 (+1.43)|
|Multilingual + fine-tuning with similarity | 31.93 (+0.19) | 36.75 (+1.62)|
|Multilingual + fine-tuning with updated embedding | **32.11 (+0.37)**| **36.74 (+1.61)**|
|Multilingual + mixing pseudo bilingual data | 30.86 (-0.88) |  35.09 (-0.04)|

### 2. French to Vietnamese (Ngo et al. 2020)

| Models     | dev | tst |
| -----------| -----| ----------------- |
| Bilingual Baseline|  23.07  | 23.03 |
| Multilingual  | 24.49 (+1.42) | 24.22 (+1.19)  |
| Multilingual + fine-tuning |24.51 (+1.44)  | 24.86 (+1.83)|
|Multilingual + fine-tuning with similarity | 24.37 (+1.30) | 24.70 (+1.63)|
|Multilingual + fine-tuning with updated embedding | 24.60 (+1.53)  | 24.96 (+1.93)|
|Multilingual + mixing pseudo bilingual data | **25.59 (+2.52)** | **25.57 (+2.54)**|
|Pseudo bilingual data translation | 19.00 | 18.71 |

### 3. Chinese to Vietnamese (Ngo et al. 2022)

| Models     | dev | tst |
| -----------| -----| ----------------- |
| Bilingual Baseline|  17.1  | 17.4 |
| ATUs data augmentation  | 17.2 (+0.1) | 17.9 (+0.5)  |
| Back Translation | 18.0 (+0.9)  | 18.5 (+1.1)|
| ATUs data augmentation + Back Translation | **18.3 (+1.2)** | 18.6 (+1.2)|
| Combine training with Japanese (ja-kytea) | 18.2 (+1.1)  | **18.7 (+1.3)**|


### 4. Japanese to Vietnamese (Ngo et al. 2022)

| Models     | dev (Ngo et al. 2018) | tst (Ngo et al. 2018)|
| -----------| -----| ----------------- |
| Bilingual Baseline (mecab)|  14.9  | 15.9 |
| ATUs data augmentation  | 18.1 (+4.1) | 19.4 (+4.0)  |
| Combined training (ja-kytea) + ATUs data augmentation | 16.8(+1.9)| 17.9(+2.0) |
| Combined training (ja-spacy) + ATUs data augmentation | 17.1 (+2.2)  | 18.6 (+2.7)|
| Combined training (ja-mecab) +ATUs data augmentation | 16.8 (+1.9)  | 18.5(+2.6)|
| Pre-trained BERT  (ja-spacy) +  Combined training +  ATUs data augmentation (ths = 7) + after 70 epochs | **23.3 (+8.4)** | **23.7 (+7.8)**|



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
and Thi-Vinh Ngo, Phuong-Thai Nguyen, Van Vinh Nguyen, Thanh-Le Ha, Le-Minh Nguyen: [An Efficient Method for Generating Synthetic Data for Low-Resource Machine Translation: An empirical study of Chinese, Japanese to Vietnamese Neural Machine Translation](https://doi.org/10.1080/08839514.2022.2101755). An International Journal: Applied Artificial Intelligence, Taylor & Francis.

Bibtex:
```
@article{doi:10.1080/08839514.2022.2101755,
author = {Thi-Vinh Ngo and Phuong-Thai Nguyen and Van Vinh Nguyen and Thanh-Le Ha and Le-Minh Nguyen},
title = {An Efficient Method for Generating Synthetic Data for Low-Resource Machine Translation},
journal = {Applied Artificial Intelligence},
volume = {36},
number = {1},
pages = {2101755},
year  = {2022},
publisher = {Taylor & Francis},
doi = {10.1080/08839514.2022.2101755},
URL = { 
        https://doi.org/10.1080/08839514.2022.2101755 
},
eprint = { 
        https://doi.org/10.1080/08839514.2022.2101755
}
}
}
```
