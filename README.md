# 이승윤 | ML Engineer 포트폴리오

K-FOOD 수출 플랫폼에서 **5개국의 품목별 수출 수요를 예측**했습니다. 직전 값과 3개월 이동평균을 기준으로 XGBoost·LightGBM 등을 비교했고, 최종 실험에서 **R² 0.991**을 기록했습니다. 국가별 유망 품목 10개를 리포트로 만드는 과정까지 맡았습니다.

해외 리뷰 10만 건으로 이진 분류(**F1 0.915**)와 등급 예측(**QWK 0.835**)을 수행했습니다. LangGraph 기반 레시피 챗봇에서는 프롬프트를 설계했고, 서비스 이용을 안내하는 도움말 챗봇은 직접 개발해 웹에 연결했습니다.

[포트폴리오 보기](https://leeseungyoons.github.io/ai-portfolio-site/) · [K-FOOD 프로젝트와 담당 역할](https://github.com/leeseungyoons/kfood-export-localization-platform#readme)

## K-FOOD 수출 수요예측

**KT AIVLE School · 2026년 1–2월 · 6인 팀, 8주**  
미국·일본·중국·베트남·독일을 대상으로 3·6·12개월 수요를 예측했습니다.

| 단계 | 실험 내용 |
| --- | --- |
| **기준 모델** | 직전 달 수출 실적을 그대로 쓰는 방법(Naive)과 최근 3개월 평균을 쓰는 방법(MA3)을 비교 기준으로 정했습니다. |
| **초기 실험** | 과거 수출 실적과 이동평균에 환율·물가지수·산업생산 지표를 결합하고, XGBoost와 LightGBM을 포함한 트리 기반 모델의 예측 성능을 비교했습니다. |
| **최종 실험** | 최종 모델의 결정계수는 **R² 0.991**이었습니다. 예측 결과를 국가별로 집계해 상위 10개 품목을 리포트에 담았습니다. |

**예측 결과의 쓰임** — 2026년 2월 결과에서 미국의 상위 세 품목은 라면, 찌거나 삶은 쌀, 쌀가루 제품이었습니다. [국가별 상위 품목 결과(JSON)](https://github.com/leeseungyoons/kfood-export-localization-platform/blob/main/ai-chatbot/forecast_top_2026_02.json)

## 리뷰 분석과 AI 서비스

| 담당한 작업 | 결과 |
| --- | --- |
| 해외 리뷰 10만 건 분석 | 이진 분류 F1 0.915, ROC-AUC 0.961. 다중 등급 예측의 가중 카파(QWK) 0.835 |
| 국가별 상위 품목 리포트 생성 | 지도·핵심 지표·SWOT·알레르기 정보를 포함한 13개 섹션 구성 |
| 레시피 챗봇 프롬프트 설계 | LangGraph와 SerpAPI를 활용해 레시피 후보를 제안하는 팀 서비스에 기여. [레시피 챗봇 코드](https://github.com/leeseungyoons/kfood-export-localization-platform/blob/main/ai-chatbot/graph.py) |
| 도움말 챗봇 개발 | 서비스 이용 절차를 안내하는 에이전트를 설계하고 웹에 연결. [도움말 챗봇 코드](https://github.com/leeseungyoons/kfood-export-localization-platform/blob/main/ai-chatbot/helper_graph.py) |

## 서비스 개발 및 배포 경험

- **백엔드 API · KT AIVLE 4차 미니프로젝트** — Spring Boot와 Next.js로 구성한 서비스에서 도서 목록 조회·상세 조회·등록 API를 담당했습니다. 데이터 저장에는 JPA와 H2를 사용했습니다.
- **AWS CI/CD · KT AIVLE 5차 미니프로젝트** — AWS CodePipeline으로 CodeBuild의 빌드 단계와 CodeDeploy의 배포 단계를 연결해 EC2의 Nginx 환경에 배포했습니다.
- **스포츠 뉴스 감정분석 · 개인 포트폴리오** — BERT로 스포츠 뉴스의 감정을 분류하고 Streamlit 화면에서 결과를 확인할 수 있도록 구현했습니다. [프로젝트 코드 보기](https://github.com/leeseungyoons/sports-news-sentiment-analysis)

## 이 저장소

포트폴리오 웹사이트를 기획하고 HTML·CSS·JavaScript로 직접 구현했습니다. 사이트에서 프로젝트별 상세 내용과 수상 이력, 연락처를 확인할 수 있습니다. 로컬에서는 별도 빌드 없이 `index.html`을 브라우저에서 열면 됩니다.
