---
title: "OpenCoder-llm/OpenCoder-llm: The Open Cookbook for Top-Tier Code Large Language Model"
source: "https://github.com/OpenCoder-llm/OpenCoder-llm"
author:
  - "[[OpenCoder-llm]]"
published:
created: 2024-11-14
description: "The Open Cookbook for Top-Tier Code Large Language Model - OpenCoder-llm/OpenCoder-llm"
tags:
  - "clippings"
---


## 오픈코더

⚡ 최상위 코드 대규모 언어 모델을 위한 오픈 쿡북 ⚡

🏠 [홈페이지](https://opencoder-llm.github.io/)    | 🤗 [모델](https://huggingface.co/collections/infly/opencoder-672cec44bbb86c39910fb55e)    | 📊 [데이터 세트](https://huggingface.co/collections/OpenCoder-LLM/opencoder-datasets-672e6db6a0fed24bd69ef1c2)    | 📄 [논문](https://arxiv.org/abs/2411.04905)   ｜ 🚀 [데모](https://huggingface.co/spaces/OpenCoder-LLM/OpenCoder-8B-Instruct)  

[![12](https://private-user-images.githubusercontent.com/55043304/384522629-3aa8dd8f-b12a-46e7-a543-d81cfd175d30.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzE1NjM4MjgsIm5iZiI6MTczMTU2MzUyOCwicGF0aCI6Ii81NTA0MzMwNC8zODQ1MjI2MjktM2FhOGRkOGYtYjEyYS00NmU3LWE1NDMtZDgxY2ZkMTc1ZDMwLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDExMTQlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQxMTE0VDA1NTIwOFomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWQyNGMwZjg2NDM0NzU3ODM0MWZkMDNkMDk2N2VlMWJkYmIyODczMTUwMjNhZmQ5MjAyZWE4MGIxNTM2Y2JjYTAmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.f2MnZ1LDKuu4eiD7kNZKdh2ou3kxkNyDXykBWXYMc48)](https://private-user-images.githubusercontent.com/55043304/384522629-3aa8dd8f-b12a-46e7-a543-d81cfd175d30.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzE1NjM4MjgsIm5iZiI6MTczMTU2MzUyOCwicGF0aCI6Ii81NTA0MzMwNC8zODQ1MjI2MjktM2FhOGRkOGYtYjEyYS00NmU3LWE1NDMtZDgxY2ZkMTc1ZDMwLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDExMTQlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQxMTE0VDA1NTIwOFomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWQyNGMwZjg2NDM0NzU3ODM0MWZkMDNkMDk2N2VlMWJkYmIyODczMTUwMjNhZmQ5MjAyZWE4MGIxNTM2Y2JjYTAmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.f2MnZ1LDKuu4eiD7kNZKdh2ou3kxkNyDXykBWXYMc48)

## 소식

- 🔥🔥 저희는 효율적인 CodeLLM 평가 프레임워크인 [OpenCodeEval을](https://github.com/OpenCoder-llm/OpenCoder-llm/tree/main/OpenCodeEval)`2024/11/12` 출시했습니다 .- 🔥🔥 우리는 algorithmic-corpus와 해당 합성 데이터를 포함하는 `2024/11/12`고품질 어닐링 데이터 📊 [opc-annealing-corpus를 공개했습니다.](https://huggingface.co/datasets/OpenCoder-LLM/opc-annealing-corpus)
- 🔥 [Fineweb](https://huggingface.co/datasets/HuggingFaceFW/fineweb)`2024/11/11` 에서 회수된 55B 페이지를 공개했습니다 . 여기에는 📊 [fineweb-code-corpus](https://huggingface.co/datasets/OpenCoder-LLM/fineweb-code-corpus) 와 📊 [fineweb-math-corpus가](https://huggingface.co/datasets/OpenCoder-LLM/fineweb-math-corpus) 포함됩니다 .- 🔥 `2024/11/09`450만 개의 훈련 후 데이터를 공개했습니다: 📊 [데이터 세트](https://huggingface.co/collections/OpenCoder-LLM/opencoder-datasets-672e6db6a0fed24bd69ef1c2) .
- 🔥 `2024/11/08`모델을 공개했습니다! 🤗 [Model](https://huggingface.co/collections/infly/opencoder-672cec44bbb86c39910fb55e) 에서 다운로드하세요 .
- 🔥 `2024/11/07`Arxiv에 논문을 공개했습니다: 📄 [OpenCoder: 최상위 코드 대규모 언어 모델을 위한 오픈 쿡북](https://arxiv.org/abs/2411.04905) .

## 출시

- 데이터 정리 파이프라인
- 중간 체크포인트
- **RefineCode** : 원시 코드 데이터의 메타데이터
- **RefineCode** : 코드 관련 웹 데이터
- CodeLLM 평가 프레임워크: OpenCodeEval
- 고품질 어닐링 데이터
- 훈련 후 데이터
- 최종 모델 무게
- 종이

저희는 모든 리소스를 공개하기 위해 열심히 노력하고 있습니다! 💪

## 소개

**OpenCoder** 는 영어와 중국어를 모두 지원하는 1.5B 및 8B 기본 및 채팅 모델을 포함하는 개방적이고 재현 가능한 코드 LLM 제품군입니다. 처음부터 OpenCoder는 90% 원시 코드와 10% 코드 관련 웹 데이터로 구성된 2.5조 토큰에서 사전 학습되었으며, 4.5M개 이상의 고품질 SFT 예제에서 미세 조정되어 최종적으로 최상위 코드 LLM의 성능에 도달했습니다. 모델 가중치와 추론 코드뿐만 아니라 재현 가능한 학습 데이터, 완전한 데이터 처리 파이프라인, 엄격한 실험적 절제 결과 및 자세한 학습 프로토콜도 제공합니다. 연구자들이 구축하고 혁신할 수 있도록 지원하는 OpenCoder는 코드 AI를 발전시키기 위한 개방형 기반입니다.

- **완전한 오픈 소스** : OpenCoder는 모델 가중치와 향후 추론 코드뿐만 아니라 학습을 위한 완전한 데이터 정리 코드도 공개하여 완전한 투명성을 보장합니다. 이 릴리스에는 고품질 합성 데이터, 광범위한 체크포인트 세트, 450만 개가 넘는 감독 미세 조정(SFT) 항목의 데이터 세트가 포함되어 OpenCoder를 가장 포괄적으로 오픈 소스화된 모델 중 하나로 만듭니다.
- **포괄적인 실험 분석** : OpenCoder는 다양한 데이터 정리 전략과 교육 프로세스에 대한 광범위한 절삭 연구를 통해 엄격하게 테스트되었으며, 여기에는 파일 수준과 저장소 수준의 중복 제거 실험이 포함되어 모델 성능에 대한 철저한 탐색과 검증이 보장됩니다.
- **고품질 합성 데이터** : OpenCoder는 완전히 개발된 합성 데이터 생성 프로세스와 450만 개 이상의 SFT 데이터 항목을 제공하여 모델 학습과 평가를 위한 강력한 데이터 기반을 구축합니다.
- **뛰어난 성능** : OpenCoder는 여러 언어 모델 벤치마크에서 높은 성능을 달성하여 코드를 위한 선도적인 오픈소스 모델 중 하나로 자리매김했습니다.

## 모델

| 모델 | 시퀀스 길이 | 허깅페이스 | 와이즈모델 |
| --- | --- | --- | --- |
| OpenCoder-1.5B-베이스 | 4K | [🤗허깅페이스](https://huggingface.co/infly/OpenCoder-1.5B-Base) | [![](https://github.com/OpenCoder-llm/opencoder-llm.github.io/raw/main/static/images/wisemodel_logo.png?raw=true)](https://wisemodel.cn/models/OpenCoder/OpenCoder-1.5B-Base) |
| 오픈코더-8B-베이스 | 8K | [🤗허깅페이스](https://huggingface.co/infly/OpenCoder-8B-Base) | [![](https://github.com/OpenCoder-llm/opencoder-llm.github.io/raw/main/static/images/wisemodel_logo.png?raw=true)](https://wisemodel.cn/models/OpenCoder/OpenCoder-8B-Base) |
| 오픈코더-1.5B-인스트럭트 | 4K | [🤗허깅페이스](https://huggingface.co/infly/OpenCoder-1.5B-Instruct) | [![](https://github.com/OpenCoder-llm/opencoder-llm.github.io/raw/main/static/images/wisemodel_logo.png?raw=true)](https://wisemodel.cn/models/OpenCoder/OpenCoder-1.5B-Instruct) |
| 오픈코더-8B-인스트럭트 | 8K | [🤗허깅페이스](https://huggingface.co/infly/OpenCoder-8B-Instruct) | [![](https://github.com/OpenCoder-llm/opencoder-llm.github.io/raw/main/static/images/wisemodel_logo.png?raw=true)](https://wisemodel.cn/models/OpenCoder/OpenCoder-8B-Instruct) |

## 데이터 세트

### 사전 훈련

| 데이터 세트 | 크기 | 다운로드 |
| --- | --- | --- |
| 파인웹-코드-코퍼스 | 148기가바이트 | [🤗허깅페이스](https://huggingface.co/datasets/OpenCoder-LLM/fineweb-code-corpus) |
| 파인웹-수학-코퍼스 | 10GB | [🤗허깅페이스](https://huggingface.co/datasets/OpenCoder-LLM/fineweb-math-corpus) |
| opc-어닐링-코퍼스 | 24GB | [🤗허깅페이스](https://huggingface.co/datasets/OpenCoder-LLM/opc-annealing-corpus) |

### 훈련 후

| 데이터 세트 | 숫자 | 다운로드 |
| --- | --- | --- |
| opc-sft-스테이지1 | 4.21만 | [🤗허깅페이스](https://huggingface.co/datasets/OpenCoder-LLM/opc-sft-stage1) |
| opc-sft-스테이지2 | 375만 | [🤗허깅페이스](https://huggingface.co/datasets/OpenCoder-LLM/opc-sft-stage2) |

**이것이 끝이 아닙니다. 남은 데이터를 정리하여 점진적으로 업로드하고 있습니다.**

## 성능

[![](https://private-user-images.githubusercontent.com/55043304/384512021-7f5a49b2-9539-4185-91fa-fd32c1315b2a.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzE1NjM4MjgsIm5iZiI6MTczMTU2MzUyOCwicGF0aCI6Ii81NTA0MzMwNC8zODQ1MTIwMjEtN2Y1YTQ5YjItOTUzOS00MTg1LTkxZmEtZmQzMmMxMzE1YjJhLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDExMTQlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQxMTE0VDA1NTIwOFomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTgzMjQ2ZmJhNDM4NjBhOWMwMGRiYWNjZWY1ZjExMGUwOTRiYzM5NTFlMTc5OGE5MDhlNjM3YThhODhlNDk2YjEmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.to6gaFhG5b4kvCWyRP1Iw996St0WPOk0jaUBDFhwmrU)](https://private-user-images.githubusercontent.com/55043304/384512021-7f5a49b2-9539-4185-91fa-fd32c1315b2a.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzE1NjM4MjgsIm5iZiI6MTczMTU2MzUyOCwicGF0aCI6Ii81NTA0MzMwNC8zODQ1MTIwMjEtN2Y1YTQ5YjItOTUzOS00MTg1LTkxZmEtZmQzMmMxMzE1YjJhLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDExMTQlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQxMTE0VDA1NTIwOFomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTgzMjQ2ZmJhNDM4NjBhOWMwMGRiYWNjZWY1ZjExMGUwOTRiYzM5NTFlMTc5OGE5MDhlNjM3YThhODhlNDk2YjEmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.to6gaFhG5b4kvCWyRP1Iw996St0WPOk0jaUBDFhwmrU) [![](https://private-user-images.githubusercontent.com/55043304/384511981-81c6e686-0ed0-4eb5-8fb8-a651750ec346.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzE1NjM4MjgsIm5iZiI6MTczMTU2MzUyOCwicGF0aCI6Ii81NTA0MzMwNC8zODQ1MTE5ODEtODFjNmU2ODYtMGVkMC00ZWI1LThmYjgtYTY1MTc1MGVjMzQ2LnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDExMTQlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQxMTE0VDA1NTIwOFomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWMxZGIyNTQ0OWMwYzgzYjQxYzYzZGJlZmU5OWQyMDIzNmUyZGJlMjk2ODFkYWNlZjJiZmQzMzk4OGIzZGE1MzkmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.uMPp1z8rjXHB-TO4EyYoRYISky85TIqpCWdK-kKS_m0)](https://private-user-images.githubusercontent.com/55043304/384511981-81c6e686-0ed0-4eb5-8fb8-a651750ec346.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzE1NjM4MjgsIm5iZiI6MTczMTU2MzUyOCwicGF0aCI6Ii81NTA0MzMwNC8zODQ1MTE5ODEtODFjNmU2ODYtMGVkMC00ZWI1LThmYjgtYTY1MTc1MGVjMzQ2LnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDExMTQlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQxMTE0VDA1NTIwOFomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWMxZGIyNTQ0OWMwYzgzYjQxYzYzZGJlZmU5OWQyMDIzNmUyZGJlMjk2ODFkYWNlZjJiZmQzMzk4OGIzZGE1MzkmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.uMPp1z8rjXHB-TO4EyYoRYISky85TIqpCWdK-kKS_m0)

## 시작하기

```
import torch
from transformers import AutoTokenizer, AutoModelForCausalLM

model_name = "infly/OpenCoder-8B-Instruct"
model = AutoModelForCausalLM.from_pretrained(model_name,
                                             torch_dtype=torch.bfloat16,
                                             device_map="auto",
                                             trust_remote_code=True)
tokenizer = AutoTokenizer.from_pretrained(model_name, trust_remote_code=True)

messages=[
    { 'role': 'user', 'content': "write a quick sort algorithm in python."}
]

inputs = tokenizer.apply_chat_template(messages, add_generation_prompt=True, return_tensors="pt")

outputs = model.generate(inputs, max_new_tokens=512, do_sample=False)

result = tokenizer.decode(outputs[0][len(inputs[0]):], skip_special_tokens=True)
print(result)
```

## 소환

만약 저희의 작업이 도움이 된다면, 인용해 주시기 바랍니다 :-)

```
@inproceedings{Huang2024OpenCoderTO,
  title={OpenCoder: The Open Cookbook for Top-Tier Code Large Language Models},
  author={Siming Huang and Tianhao Cheng and Jason Klein Liu and Jiaran Hao and Liuyihan Song and Yang Xu and J. Yang and J. H. Liu and Chenchen Zhang and Linzheng Chai and Ruifeng Yuan and Zhaoxiang Zhang and Jie Fu and Qian Liu and Ge Zhang and Zili Wang and Yuan Qi and Yinghui Xu and Wei Chu},
  year={2024},
  url={https://arxiv.org/pdf/2411.04905}
}
```

## 별의 역사

[![별의 역사 차트](https://camo.githubusercontent.com/bb6775150d312fbf030928b7793d5396ddcaa809e8b638d19d99c235ad8d5651/68747470733a2f2f6170692e737461722d686973746f72792e636f6d2f7376673f7265706f733d4f70656e436f6465722d6c6c6d2f4f70656e436f6465722d6c6c6d26747970653d44617465)](https://star-history.com/#OpenCoder-llm/OpenCoder-llm&Date)