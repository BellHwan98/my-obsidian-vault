# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Obsidian vault ("Kevin Kim") synced via iCloud. '지식 발전소(Zettelkasten)'와 '프로젝트 작업대(PARA)'를 분리하는 이중 구조로 운영한다. AI 도구(Claude, Ollama, OpenRouter), Zotero, n8n과 통합.

## Vault Structure

```
0. Docs/                     - Claude Code + Obsidian 운영 참고 문서
Projects/                    - 마감일 있는 프로젝트 (완료 → Archive)
Areas/                       - 지속적 관리 영역 (English, 건강, 커리어 등)
Resources/                   - 주제별 참고 자료 (범용, 프로젝트 무관)
Archive/                     - 완료된 항목 보관 (원본 구조 유지)
Zettelkasten/
├── 00. Inbox/               - 빠른 캡처, 아이디어 씨앗
├── 10. Literature/          - 원천 자료 요약 (논문, 책, 강의)
└── 20. Permanent/           - 자신의 언어로 정제된 영구 지식
Templates/                   - 노트 템플릿
Attachments/                 - 첨부 파일 (이미지, PDF)
```

각 폴더의 상세 규칙은 해당 폴더의 `claude.md` 참조.

## 핵심 철학: PARA vs Zettelkasten 분리

- **PARA (Projects/Areas/Resources/Archive):** 행동과 프로젝트 관리용. 시간에 따라 생성되고 완료되고 보관됨.
- **Zettelkasten:** 지식 축적용. 프로젝트가 끝나도 지식은 영구 보존. Archive로 이동하지 않음.
- 프로젝트 작업 중 얻은 지식 → Zettelkasten에 영구 노트로 분리하고 `[[]]`로 참조.

## Note Templates

표준 헤더 (template at `Templates/`):

```markdown
### 날짜: {{date: YYYY-MM-DD}}, {{time}}
### 주제:
### 테그:
---
### 메모
[content]
### 출처(참고문헌)
-
### 연결 문서
-
```

학술 노트는 확장 템플릿 사용: 핵심 개념, Title & Abstract, Introduction, Methods, Results, Discussion, Conclusion.

## Obsidian Conventions

- **Links:** Wiki-style `[[문서명]]` (Markdown 링크 사용 금지)
- **Images:** `![[파일명]]`으로 임베드
- **Attachments:** `Attachments/` 폴더에 저장
- **Naming:** `YYYY-MM-DD 키워드.md` (날짜 기반 노트)
- **Language:** Korean primary, English for academic/IELTS content
- **Theme:** Obsidianite

## Key Plugins

- **dataview** - 동적 노트 목록 쿼리
- **obsidian-textgenerator-plugin** - AI 텍스트 생성
- **obsidian-zotero-desktop-connector** / **obsidian-citation-plugin** - Zotero 참고문헌 관리
- **execute-code** - 노트 내 코드 실행
- **obsidian-excalidraw-plugin** - 다이어그램
- **obsidian-kanban** - 칸반 보드
- **terminal** - 통합 터미널

## AI/Smart Environment

- **Embedding:** TaylorAI/bge-micro-v2 (transformers)
- **Chat:** Ollama (local) + OpenRouter fallback
- **Context format:** XML-structured
- Config: `.smart-env/smart_env.json`

## Zotero References

`Zettelkasten/10. Literature/` 또는 `자료/zotero/`에 `@AuthorEtAlYear.md` 형식으로 저장.

## Legacy Folders

기존 한국어 PARA 폴더(`1. Project_마감필요/`, `2. Area_지속 관리/`, `3. Resource_언제가 필요함/`, `4. Archieve_완료 및 저장/`, `<Inbox>/`, `Clippings/`, `Files/`, `자료/`)는 점진적으로 새 구조로 마이그레이션 예정.
