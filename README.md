# 이승윤 | ML Engineer · AI 서비스 개발

K-FOOD 수출 플랫폼에서 **5개국의 품목별 수요를 예측하고, 국가별 상위 10개 품목을 리포트로 만드는 과정**을 맡았습니다. 수요예측 최종 모델의 R²는 **0.991**, 해외 리뷰 10만 건의 이진 분류 F1은 **0.915**였습니다. 같은 서비스에서 이용 절차를 안내하는 도움말 챗봇을 개발해 웹에 연결했습니다.

[포트폴리오](https://leeseungyoons.github.io/ai-portfolio-site/) · [이메일](mailto:lieme980@gmail.com) · [GitHub](https://github.com/leeseungyoons)

## 대표 프로젝트 · K-FOOD 수출 및 현지화 지원 플랫폼

**KT AIVLE School · 2026년 1–2월 · 6인 팀 · 8주**

식품 기업이 수출 후보 품목을 고르고 현지 소비자 반응을 살펴볼 수 있도록 만든 서비스입니다. [프로젝트 개요 및 팀원별 담당 업무](https://github.com/leeseungyoons/kfood-export-localization-platform#readme)

### 수출 수요예측

미국·일본·중국·베트남·독일의 품목별 수요를 3·6·12개월 단위로 예측했습니다. 과거 수출 실적에서 시차와 이동평균을 계산하고 환율·물가지수·산업생산 지표를 결합해 XGBoost와 LightGBM 등 트리 기반 모델을 비교했습니다.

| 실험 단계 | R² |
| --- | ---: |
| 초기 모델 | 약 0.84 |
| 최종 모델 | **0.991** |

예측 결과를 국가별로 집계해 상위 10개 품목을 추렸습니다. 2026년 2월 미국 목록에는 라면·김치·고추장이 포함됐습니다. [5개국 품목별 예측 결과](https://github.com/leeseungyoons/kfood-export-localization-platform/blob/main/ai-chatbot/forecast_top_2026_02.json)

### 해외 리뷰 분석과 리포트

- **리뷰 분석** — 해외 리뷰 10만 건을 두 가지 과제로 평가했습니다. 이진 분류에서는 F1 **0.915**, ROC-AUC **0.961**을 기록했고, 여러 등급을 예측하는 과제에서는 실제 등급과 예측 등급의 일치도(QWK)가 **0.835**였습니다.
- **리포트 생성** — 국가별 상위 품목을 리포트로 만드는 파이프라인을 구축했습니다. 시장 요약, 핵심 지표, SWOT, 알레르기 정보 등을 13개 섹션으로 구성했습니다.

### LangGraph 챗봇

- **도움말 챗봇** — 화면과 메뉴별 이용 절차를 정리한 문서를 바탕으로 사용자 질문에 답하는 에이전트를 설계·개발하고 웹에 연결했습니다. [도움말 에이전트 코드](https://github.com/leeseungyoons/kfood-export-localization-platform/blob/main/ai-chatbot/helper_graph.py)
- **레시피 챗봇** — 팀의 레시피 생성 기능에서 프롬프트 설계를 담당했습니다. LangGraph와 SerpAPI를 활용해 현지 트렌드를 검색하고 레시피 후보를 제시하는 흐름입니다. [레시피 생성 코드](https://github.com/leeseungyoons/kfood-export-localization-platform/blob/main/ai-chatbot/graph.py)

## 다른 개발 경험

- **야구 뉴스 감정분석** — 야구 기사를 업로드하면 긍정·부정 분포와 핵심 키워드를 확인할 수 있는 Streamlit 앱을 구현했습니다. ‘역전승’, ‘병살타’처럼 야구 문맥에서 감정이 드러나는 표현을 분류 로직에 반영했습니다. [분류 코드](https://github.com/leeseungyoons/sports-news-sentiment-analysis/blob/main/sentiment_model.py)
- **도서 관리 API** — KT AIVLE 4차 미니프로젝트에서 도서 등록·목록 조회·상세 조회 API를 담당했습니다. Spring Boot와 JPA로 구현하고 Next.js 화면과 연동했습니다. [도서 관리 프로젝트](https://github.com/leeseungyoons/ai-bookshelf-service)
- **AWS CI/CD** — KT AIVLE 5차 미니프로젝트에서 CodePipeline으로 CodeBuild의 빌드와 CodeDeploy의 배포를 연결해 EC2의 Nginx 환경에 배포했습니다.

## 포트폴리오 사이트

HTML·CSS·JavaScript로 만든 반응형 사이트입니다. 프로젝트 상세 내용과 수상 이력은 [포트폴리오](https://leeseungyoons.github.io/ai-portfolio-site/)에서 볼 수 있습니다. 로컬에서는 `index.html`을 브라우저로 열면 됩니다.
