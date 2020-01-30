# HanBert-NER

- HanBert 이용한 한국어 Named Entity Recognition Task
- `Huggingface Tranformers` 라이브러리를 이용하여 구현

## Dependencies

- torch>=1.1.0
- transformers>=2.2.2
- seqeval>=0.0.12
- sentencepiece>=0.1.82

## Dataset

- **Naver NLP Challenge 2018**의 NER Dataset 사용 ([Github link](https://github.com/naver/nlp-challenge))
- 해당 데이터셋에 Train dataset만 존재하기에, Test dataset은 Train dataset에서 split하였습니다. ([Data link](https://github.com/aisolab/nlp_implementation/tree/master/Bidirectional_LSTM-CRF_Models_for_Sequence_Tagging/data))
  - Train (81,000) / Test (9,000)

## Usage

```bash
$ python3 main.py --model_type hanbert --model_name_or_path HanBert-54kN-torch --do_train --do_eval
```

## Results

|                   | Slot F1 (%) |
| ----------------- | ----------- |
| HanBert-54kN      | 84.84       |
| HanBert-54kN-IP   |             |
| KoBERT            | 84.23       |
| DistilKoBERT      | 82.14       |
| Bert-Multilingual | 81.78       |
| BiLSTM-CRF        | 76.45       |

## References

- [HanBert](https://github.com/tbai2019/HanBert-54k-N)
- [Naver NLP Challenge](https://github.com/naver/nlp-challenge)
- [Huggingface Transformers](https://github.com/huggingface/transformers)
- [NLP Implementation by aisolab](https://github.com/aisolab/nlp_implementation)
- [BERT NER by eagle705](https://github.com/eagle705/pytorch-bert-crf-ner)
