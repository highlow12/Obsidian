---
title: "glowingjade/obsidian-smart-composer: AI chat assistant for Obsidian with contextual awareness, smart writing assistance, and one-click edits. Features vault-aware conversations, semantic search, and local model support."
source: https://github.com/glowingjade/obsidian-smart-composer
author:
  - "[[GitHub]]"
  - glowingjade
published: 
created: 2024-11-28
description: AI chat assistant for Obsidian with contextual awareness, smart writing assistance, and one-click edits. Features vault-aware conversations, semantic search, and local model support. - glowingjade/obsidian-smart-composer
tags:
  - clippings
---
## 요약

Smart Composer는 Obsidian에서 AI 기반 글쓰기를 위한 강력한 도구입니다. 컨텍스트 채팅, 편집 적용, 볼트 검색(RAG) 등의 주요 기능을 통해 효율적인 콘텐츠 생성을 지원합니다. 멀티미디어 컨텍스트 지원으로 웹사이트 링크 및 YouTube 대본을 활용할 수 있으며, 향후 이미지 및 외부 파일 지원도 예정되어 있습니다. 사용자 정의 모델 선택, 로컬 모델 지원, 사용자 정의 시스템 프롬프트, 프롬프트 템플릿 등 다양한 추가 기능도 제공합니다. 자세한 내용은 문서 및 GitHub 프로젝트 칸반 보드를 참조하십시오.

## 스마트 컴포저

[문서](https://github.com/glowingjade/obsidian-smart-composer/wiki) · [버그 보고](https://github.com/glowingjade/obsidian-smart-composer/issues) · [토론](https://github.com/glowingjade/obsidian-smart-composer/discussions)

ChatGPT에 질문할 때마다 각 쿼리에 대해 많은 컨텍스트 정보를 입력해야 합니다. 왜 이미 볼트에 있는 배경 정보를 입력하는 데 시간을 허비합니까?

**Smart Composer는 AI로 효율적으로 글을 쓸 수 있도록 도와주는 Obsidian 플러그인으로, 볼트 콘텐츠를 쉽게 참조할 수 있습니다.** Cursor AI와 ChatGPT Canvas에서 영감을 받은 이 플러그인은 Obsidian 내에서 노트 작성 및 콘텐츠 생성 프로세스를 통합합니다.

## 특징

### 컨텍스트 채팅

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

> Smart Composer는 **문서에 대한 편집을 제안합니다.** 한 번의 클릭으로 적용할 수 있습니다.

- 문서 변경 권장 사항을 제공합니다
- 제안된 변경 사항을 즉시 적용합니다

참고: Apply Edit 기능은 현재 원하는 것보다 느립니다. 향후 업데이트에서 개선을 위해 노력하고 있습니다.

### 볼트 검색(RAG)

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
```
