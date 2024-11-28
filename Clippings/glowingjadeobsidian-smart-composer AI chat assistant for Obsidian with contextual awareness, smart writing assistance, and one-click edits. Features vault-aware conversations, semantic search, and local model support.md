---
title: "glowingjade/obsidian-smart-composer: AI chat assistant for Obsidian with contextual awareness, smart writing assistance, and one-click edits. Features vault-aware conversations, semantic search, and local model support."
source: "https://github.com/glowingjade/obsidian-smart-composer"
author:
  - "[[GitHub]]"
published:
created: 2024-11-28
description: "AI chat assistant for Obsidian with contextual awareness, smart writing assistance, and one-click edits. Features vault-aware conversations, semantic search, and local model support. - glowingjade/obsidian-smart-composer"
tags:
  - "clippings"
---
## 스마트 컴포저

[문서](https://github.com/glowingjade/obsidian-smart-composer/wiki) · [버그 보고](https://github.com/glowingjade/obsidian-smart-composer/issues) · [토론](https://github.com/glowingjade/obsidian-smart-composer/discussions)

[![SC1_제목.gif](https://private-user-images.githubusercontent.com/18643499/376500532-a50a1f80-39ff-4eba-8090-e3d75e7be98c.gif?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzI4MDUzNDksIm5iZiI6MTczMjgwNTA0OSwicGF0aCI6Ii8xODY0MzQ5OS8zNzY1MDA1MzItYTUwYTFmODAtMzlmZi00ZWJhLTgwOTAtZTNkNzVlN2JlOThjLmdpZj9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDExMjglMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQxMTI4VDE0NDQwOVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWZiYzczNzYwZTg3NzQ0NDBhNDQ2MzAzY2U2Njc4ZmI0MGRkYzNiNWI1Y2E1Yjg0NmQ0MzkxMzBmNjk4NzJhYWUmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.U4JDOw6Jc0w48N2bfJxxzUuysKYY_IiPBRDh79hLqPE)](https://private-user-images.githubusercontent.com/18643499/376500532-a50a1f80-39ff-4eba-8090-e3d75e7be98c.gif?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzI4MDUzNDksIm5iZiI6MTczMjgwNTA0OSwicGF0aCI6Ii8xODY0MzQ5OS8zNzY1MDA1MzItYTUwYTFmODAtMzlmZi00ZWJhLTgwOTAtZTNkNzVlN2JlOThjLmdpZj9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDExMjglMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQxMTI4VDE0NDQwOVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWZiYzczNzYwZTg3NzQ0NDBhNDQ2MzAzY2U2Njc4ZmI0MGRkYzNiNWI1Y2E1Yjg0NmQ0MzkxMzBmNjk4NzJhYWUmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.U4JDOw6Jc0w48N2bfJxxzUuysKYY_IiPBRDh79hLqPE)

ChatGPT에 질문할 때마다 각 쿼리에 대해 많은 컨텍스트 정보를 입력해야 합니다. 왜 이미 볼트에 있는 배경 정보를 입력하는 데 시간을 허비합니까?

**Smart Composer는 AI로 효율적으로 글을 쓸 수 있도록 도와주는 Obsidian 플러그인으로, 볼트 콘텐츠를 쉽게 참조할 수 있습니다.** Cursor AI와 ChatGPT Canvas에서 영감을 받은 이 플러그인은 Obsidian 내에서 노트 작성 및 콘텐츠 생성 프로세스를 통합합니다.

## 특징

### 컨텍스트 채팅

[![SC2_컨텍스트채팅.gif](https://private-user-images.githubusercontent.com/18643499/376500555-8da4c189-399a-450a-9591-95f1c9af1bc8.gif?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzI4MDUzNDksIm5iZiI6MTczMjgwNTA0OSwicGF0aCI6Ii8xODY0MzQ5OS8zNzY1MDA1NTUtOGRhNGMxODktMzk5YS00NTBhLTk1OTEtOTVmMWM5YWYxYmM4LmdpZj9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDExMjglMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQxMTI4VDE0NDQwOVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTc1ODM4NDc3YWYyMTYxMGQ5ODZiNWJlZTQ0MGEyZmNhOTg4NWMwNGFjZjNiODViN2M3MjI0MmFkNDk4Mzc1YzYmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.wwoBOVkv7Mm1Sk5_qvCork0wWytLNkhz19m7vw0ULHE)](https://private-user-images.githubusercontent.com/18643499/376500555-8da4c189-399a-450a-9591-95f1c9af1bc8.gif?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzI4MDUzNDksIm5iZiI6MTczMjgwNTA0OSwicGF0aCI6Ii8xODY0MzQ5OS8zNzY1MDA1NTUtOGRhNGMxODktMzk5YS00NTBhLTk1OTEtOTVmMWM5YWYxYmM4LmdpZj9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDExMjglMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQxMTI4VDE0NDQwOVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTc1ODM4NDc3YWYyMTYxMGQ5ODZiNWJlZTQ0MGEyZmNhOTg4NWMwNGFjZjNiODViN2M3MjI0MmFkNDk4Mzc1YzYmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.wwoBOVkv7Mm1Sk5_qvCork0wWytLNkhz19m7vw0ULHE)

> Cursor AI에서 영감을 받은 Contextual AI Assistant로 노트 작성 경험을 업그레이드하세요. 일반적인 AI 플러그인과 달리, 저희의 Assistant를 사용하면 **대화의 맥락을 정확하게 선택할 수 있습니다.**

- `@<fname>`대화 맥락으로 특정 파일/폴더를 선택하려면 입력하세요.
- 선택한 볼트 콘텐츠에 따라 응답을 받으세요

#### 멀티미디어 컨텍스트

[![SC2-2_멀티컨텍스트.png](https://private-user-images.githubusercontent.com/43122135/380013658-b22175d4-80a2-4122-8555-2b9dd4987f93.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzI4MDUzNDksIm5iZiI6MTczMjgwNTA0OSwicGF0aCI6Ii80MzEyMjEzNS8zODAwMTM2NTgtYjIyMTc1ZDQtODBhMi00MTIyLTg1NTUtMmI5ZGQ0OTg3ZjkzLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDExMjglMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQxMTI4VDE0NDQwOVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWRmZmQ2ZThjMTY0ZDliNjZiZDUyNjAwNzQ4YTAyYTU0MmM5NGU0YTI1ODFmYzY0ZGQ0OGJhNTVhMTQ1YzVkZjEmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.H3RQA8N4vHEumZaFokr-byaXVPr-iMMG5meMMvNrLCU)](https://private-user-images.githubusercontent.com/43122135/380013658-b22175d4-80a2-4122-8555-2b9dd4987f93.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzI4MDUzNDksIm5iZiI6MTczMjgwNTA0OSwicGF0aCI6Ii80MzEyMjEzNS8zODAwMTM2NTgtYjIyMTc1ZDQtODBhMi00MTIyLTg1NTUtMmI5ZGQ0OTg3ZjkzLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDExMjglMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQxMTI4VDE0NDQwOVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWRmZmQ2ZThjMTY0ZDliNjZiZDUyNjAwNzQ4YTAyYTU0MmM5NGU0YTI1ODFmYzY0ZGQ0OGJhNTVhMTQ1YzVkZjEmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.H3RQA8N4vHEumZaFokr-byaXVPr-iMMG5meMMvNrLCU)

이제 귀하의 질의에 대한 추가 맥락을 제공하기 위해 **웹사이트 링크를 추가 할 수 있습니다.**

- 웹사이트 콘텐츠가 자동으로 추출됩니다
- **Youtube 링크 지원** : YouTube 대본을 가져와 컨텍스트로 포함합니다.
- **곧 출시** : 이미지 및 외부 파일(PDF, DOCX, ...) 지원

### 편집 적용

[![SC3_ApplyEdit.gif](https://private-user-images.githubusercontent.com/18643499/376500560-35ee03ff-4a61-4d08-8032-ca61fb37dcf1.gif?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzI4MDUzNDksIm5iZiI6MTczMjgwNTA0OSwicGF0aCI6Ii8xODY0MzQ5OS8zNzY1MDA1NjAtMzVlZTAzZmYtNGE2MS00ZDA4LTgwMzItY2E2MWZiMzdkY2YxLmdpZj9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDExMjglMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQxMTI4VDE0NDQwOVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWNlNTg3OGIyZGJhM2Y4MTljNjY0MWVhYjI1MDMwMGUzMGIyZDY2ZDJmYWJjNzMxZmFjNmI2ODY4OGRiM2ZkMzcmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.-W6H3ZBhJ2wkAx6nxvUKKFMcks_RJMcpX3h4MTU17vI)](https://private-user-images.githubusercontent.com/18643499/376500560-35ee03ff-4a61-4d08-8032-ca61fb37dcf1.gif?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzI4MDUzNDksIm5iZiI6MTczMjgwNTA0OSwicGF0aCI6Ii8xODY0MzQ5OS8zNzY1MDA1NjAtMzVlZTAzZmYtNGE2MS00ZDA4LTgwMzItY2E2MWZiMzdkY2YxLmdpZj9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDExMjglMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQxMTI4VDE0NDQwOVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWNlNTg3OGIyZGJhM2Y4MTljNjY0MWVhYjI1MDMwMGUzMGIyZDY2ZDJmYWJjNzMxZmFjNmI2ODY4OGRiM2ZkMzcmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.-W6H3ZBhJ2wkAx6nxvUKKFMcks_RJMcpX3h4MTU17vI)

> Smart Composer는 **문서에 대한 편집을 제안합니다.** 한 번의 클릭으로 적용할 수 있습니다.

- 문서 변경 권장 사항을 제공합니다
- 제안된 변경 사항을 즉시 적용합니다

참고: Apply Edit 기능은 현재 원하는 것보다 느립니다. 향후 업데이트에서 개선을 위해 노력하고 있습니다.

### 볼트 검색(RAG)

[![SC4_RAG-ezgif.com-crop-video.gif](https://private-user-images.githubusercontent.com/43122135/380013647-91c3ab8d-56d7-43b8-bb4a-1e73615a40ec.gif?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzI4MDUzNDksIm5iZiI6MTczMjgwNTA0OSwicGF0aCI6Ii80MzEyMjEzNS8zODAwMTM2NDctOTFjM2FiOGQtNTZkNy00M2I4LWJiNGEtMWU3MzYxNWE0MGVjLmdpZj9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDExMjglMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQxMTI4VDE0NDQwOVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWQzMWUzMTZmMDI0MjBiMTQ5NTFjOTFlNDNkYjZiNTk3NTRhNGI1MTRjMWI4ZDQ5ZGViNjlhOWU1MmE1MWI3YzkmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.ttLXMf5AhE_q1b1xJYNudUpDAwt6ljeA_00WOo2bSxs)](https://private-user-images.githubusercontent.com/43122135/380013647-91c3ab8d-56d7-43b8-bb4a-1e73615a40ec.gif?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzI4MDUzNDksIm5iZiI6MTczMjgwNTA0OSwicGF0aCI6Ii80MzEyMjEzNS8zODAwMTM2NDctOTFjM2FiOGQtNTZkNy00M2I4LWJiNGEtMWU3MzYxNWE0MGVjLmdpZj9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDExMjglMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQxMTI4VDE0NDQwOVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWQzMWUzMTZmMDI0MjBiMTQ5NTFjOTFlNDNkYjZiNTk3NTRhNGI1MTRjMWI4ZDQ5ZGViNjlhOWU1MmE1MWI3YzkmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.ttLXMf5AhE_q1b1xJYNudUpDAwt6ljeA_00WOo2bSxs)

> 보관소에서 **관련 메모를 자동으로 찾아 활용하여 AI 대응을 강화하세요.**

- `Cmd+Shift+Enter`Vault Search 답변을 실행하려면 누르십시오.
- 보관소에서 의미 검색을 통해 가장 관련성 있는 컨텍스트를 찾으세요

#### 추가 기능

- **사용자 정의 모델 선택** : API 키(로컬에 저장됨)를 설정하여 고유한 모델을 사용합니다.
- **로컬 모델 지원 :** [Ollama를](https://ollama.ai/) 사용하여 오픈소스 LLM 및 임베딩 모델을 로컬에서 실행하여 완벽한 개인 정보 보호와 오프라인 사용을 보장합니다.
- **사용자 정의 시스템 프롬프트** : 모든 채팅 대화에 적용될 시스템 프롬프트를 정의하세요.
- **프롬프트 템플릿**`/` : 채팅 뷰에 입력하여 일반적인 질의에 대한 템플릿을 만들고 재사용합니다 . 반복적인 작업을 표준화하는 데 적합합니다.
- 한 번의 클릭으로 선택한 텍스트에서 템플릿을 만듭니다.

## 시작하기

> **⚠️중요: 설치 프로그램 버전 요구 사항**  
> Smart Composer에는 최신 버전의 Obsidian 설치 프로그램이 필요합니다. 플러그인이 제대로 로드되지 않는 문제가 발생하는 경우:
> 
> 1. 먼저, Obsidian을 정상적으로 업데이트해 보세요 `Settings > General > Check for updates`.
> 2. 문제가 지속되면 Obsidian 설치 프로그램을 수동으로 업데이트하세요.
> 
> - [Obsidian 다운로드 페이지](https://obsidian.md/download) 에서 최신 설치 프로그램을 다운로드하세요> - Obsidian을 완전히 닫습니다
> - 새로운 설치 프로그램을 실행합니다

1. Obsidian 설정 열기
2. "커뮤니티 플러그인"으로 이동하여 "찾아보기"를 클릭합니다.
3. "Smart Composer"를 검색하고 설치를 클릭하세요.
4. 커뮤니티 플러그인에서 플러그인을 활성화하세요
5. 플러그인 설정에서 API 키를 설정하세요
- OpenAI : [ChatGPT API 키](https://platform.openai.com/api-keys)
- Anthropic : [Claude API 키](https://console.anthropic.com/settings/keys)
- Gemini : [Gemini API 키](https://aistudio.google.com/apikey)
- Groq : [Groq API 키](https://console.groq.com/keys)

> **💡 무료 옵션 제공** : Gemini API는 속도 제한이 있지만 Smart Composer의 무료 모델 중에서 가장 뛰어난 성능을 제공합니다. 무료 옵션을 찾는 사용자에게 권장됩니다.

**📚 자세한 설정 지침과 설명서는 [설명서](https://github.com/glowingjade/obsidian-smart-composer/wiki) 에서 확인하세요 .**

## 로드맵

최신 프로젝트 로드맵과 진행 상황을 보려면 [GitHub 프로젝트 칸반 보드를](https://github.com/glowingjade/obsidian-smart-composer/projects?query=is%3Aopen) 확인하세요 .

계획된 기능 중 일부는 다음과 같습니다.

- 이미지 입력이나 외부 파일(PDF, DOCX 등) 지원
- 태그 또는 기타 메타데이터로 언급

## 피드백 및 지원

귀하의 의견을 소중히 여기며 귀하가 쉽게 생각을 공유하고 문제를 보고할 수 있도록 하고자 합니다.

- **버그 리포트** : 버그나 예상치 못한 동작이 발생하면 [GitHub Issues](https://github.com/glowingjade/obsidian-smart-composer/issues) 페이지에 문제를 제출하세요. 문제를 재현하고 해결하는 데 도움이 되도록 가능한 한 자세한 내용을 포함하세요.
- **기능 요청 : 새로운 기능 아이디어나 개선 사항이 있으면** [GitHub Discussions - Ideas & Feature Requests](https://github.com/glowingjade/obsidian-smart-composer/discussions/categories/ideas-feature-requests) 페이지를 사용하세요 . 새로운 토론을 만들어 제안을 공유하세요. 이를 통해 커뮤니티 참여가 가능하고 향후 개발의 우선순위를 정하는 데 도움이 됩니다.
- **Show and Tell : 여러분이 Smart Composer를 어떻게 사용하는지 보는 것을 좋아합니다!** [GitHub Discussions - Smart Composer Showcase](https://github.com/glowingjade/obsidian-smart-composer/discussions/categories/smart-composer-showcase) 페이지 에서 플러그인의 고유한 사용 사례, 워크플로 또는 흥미로운 응용 프로그램을 공유하세요 .

여러분의 피드백과 경험은 모든 사람을 위해 Smart Composer를 더욱 개선하는 데 매우 중요합니다!

## 기여하다

버그 리포트, 버그 수정, 문서 개선, 기능 향상 등 Smart Composer에 대한 모든 종류의 기여를 환영합니다.

**주요 기능에 대한 아이디어가 있으시면 먼저 이슈를 생성하여 실현 가능성과 구현 방법을 논의해 주세요.**

기여에 관심이 있으시다면 [CONTRIBUTING.md](https://github.com/glowingjade/obsidian-smart-composer/blob/main/CONTRIBUTING.md) 파일을 참조하여 자세한 내용을 확인하세요.

- 개발 환경 설정
- 우리의 개발 워크플로
- 데이터베이스 스키마 작업
- 풀 리퀘스트 제출 프로세스
- 개발자를 위한 알려진 문제 및 솔루션

## 특허

이 프로젝트는 [MIT 라이선스](https://github.com/glowingjade/obsidian-smart-composer/blob/main/LICENSE) 에 따라 라이선스가 부여되었습니다 .

## 프로젝트 지원하기

Smart Composer가 가치 있다고 생각되면 개발을 지원하는 것을 고려하세요.

[![나에게 커피 한 잔 사줘](https://private-user-images.githubusercontent.com/18643499/380204548-e794767d-b7dd-40eb-9132-e48ae7088000.svg?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzI4MDUzNDksIm5iZiI6MTczMjgwNTA0OSwicGF0aCI6Ii8xODY0MzQ5OS8zODAyMDQ1NDgtZTc5NDc2N2QtYjdkZC00MGViLTkxMzItZTQ4YWU3MDg4MDAwLnN2Zz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDExMjglMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQxMTI4VDE0NDQwOVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWMwZDIxMjE0NTE3OWM2YWM4OWRiMmMyMmEzOTc1YWNlYzM5YTI3NDY0MDg3N2IzNzkwZjE0YTk4OGRmMTViM2MmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.zfnJiX8BhSCQUa2xfC0_HAoZObJjFoLJbwtPZU-kbTw)](https://www.buymeacoffee.com/glowingjade)

최신 소식과 공지 사항을 받아보려면 X(Twitter) [@andy\_suh\_](https://x.com/andy_suh_) 에서 저를 팔로우하세요 !

귀하의 지원은 이 플러그인을 유지하고 개선하는 데 도움이 됩니다. 모든 기여는 감사하게 생각되며 변화를 만들어냅니다. 귀하의 지원에 감사드립니다!

## 별의 역사

[![별의 역사 차트](https://camo.githubusercontent.com/9d339cc6ee7fb0406af56554e2e2dab80e2bab69489bf5b14be0be94b24c6cf2/68747470733a2f2f6170692e737461722d686973746f72792e636f6d2f7376673f7265706f733d676c6f77696e676a6164652f6f6273696469616e2d736d6172742d636f6d706f73657226747970653d44617465)](https://star-history.com/#glowingjade/obsidian-smart-composer&Date)