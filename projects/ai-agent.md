# AI Agent 분석 플랫폼

암호화폐 뉴스와 가격 데이터를 함께 조회하여 특정 시점의 가격을 분석하는 AI Agent 프로젝트입니다. 데이터 수집부터 검색, 질의 분석, 도구 선택, 응답 생성까지 이어지는 흐름을 구현했습니다.

[포트폴리오 목록으로 돌아가기](../README.md)

## 개발 범위

1인 프로젝트로 뉴스 수집 파이프라인, Python·FastAPI 서버, LangChain 기반 RAG 및 에이전트 처리 흐름을 개발했습니다.

## 주요 구현 내용

- **데이터 수집 자동화:** 과거 뉴스 확보의 제약을 해결하기 위해 Selenium 크롤러를 구현했습니다. 원문 수집, 문서 청크 분할·임베딩, ChromaDB 저장으로 이어지는 파이프라인을 구성했습니다.
- **RAG 기반 분석:** ChromaDB의 의미 검색 결과와 가격 데이터를 활용하여 분석문을 생성하도록 구현했습니다.
- **질의 분석과 도구 선택:** Query Analyzer로 자연어 질문의 코인·날짜 정보를 구조화하고, Query Planner가 가격 데이터와 뉴스 임베딩 조회 도구를 선택한 뒤 실행 결과를 통합하도록 구성했습니다.
- **멀티턴 대화:** 서버의 단기 메모리에 세션별 대화 이력을 저장하고, Entry Agent가 이를 참조하여 응답 경로를 결정하도록 개선했습니다.
- **배치 실행:** PowerShell과 Windows 작업 스케줄러를 활용해 데이터 수집 및 임베딩 작업을 실행했습니다.

## 기술

Python, FastAPI, LangChain, Selenium, ChromaDB, MongoDB, OpenAI, Claude, PowerShell, Windows 작업 스케줄러

## 소스 코드

| 구성 | 저장소 | 내용 |
| --- | --- | --- |
| AI Agent 및 서버 | [coin-news](https://github.com/keyveloper/coin-news) | Python 애플리케이션, 에이전트·RAG 처리, 크롤러 실행 코드 |
| 배치 자동화 | [coin-news-batch](https://github.com/keyveloper/coin-news-batch) | 가격·뉴스 수집과 임베딩 작업을 실행하는 PowerShell 스크립트 |

## 개선 과제

분석 결과에 대한 평가, 프롬프트·입력 토큰 최적화, 장기 기억 적용을 개선 과제로 정리했습니다.
