# 조동휘 · 신입 백엔드 개발자

Java·Spring Boot로 백엔드를 개발하고 있습니다. 생활의 불편에서 출발해 장치·서버·앱을 연결했고, 구현한 동작을 테스트와 실행 기록으로 설명하는 데 집중하고 있습니다.

`Java` `Spring Boot` `Spring MVC` `JDBC` `Python` `Django` `Flask`

## 백엔드 코드부터 확인하기

| 프로젝트 | 확인할 구현 | 현재 상태 |
| :--- | :--- | :--- |
| [Minuet](https://github.com/ZANDHIFORCE/Minuet_project) | 계층 분리, 메모리·JDBC 저장소 교체, 정상·예외 테스트 | 개인 프로젝트 · 개선 중 |
| [Urination Detector](https://github.com/ZANDHIFORCE/UrinationDetector) | 이미지 저장·조회·라벨 API, Android·장치 연동 | 수집·연동·현장 시연 프로토타입 |
| [AI Trainer](https://github.com/ZANDHIFORCE/AITrainer) | Flask 요청 처리, 외부 AI API 호출, 결과 화면 | 서비스 구현·연구 평가 |

### Minuet · Java와 데이터 접근

학생·강사·레슨 관리의 Controller·Service·Repository 책임을 나누고, 저장소 인터페이스에 메모리·JDBC 구현을 연결했습니다. 서비스·저장소·컨트롤러의 정상 동작과 예외 상황을 테스트로 표현했습니다.

H2 초기화와 테스트 준비 오류를 수정한 [보완 PR](https://github.com/ZANDHIFORCE/Minuet_project/pull/2)에서 **기존 테스트 141개 통과**와 실제 HTTP 등록·조회를 확인했습니다. 이 결과는 해당 PR 브랜치 기준이며 기본 브랜치 반영 전입니다. 학원에 도입·운영한 서비스는 아닙니다.

[서비스 테스트](https://github.com/ZANDHIFORCE/Minuet_project/blob/main/src/test/java/com/ZandhiDokkie/minuet/service/StudentServiceTest.java) · [PR 검증 기록](https://github.com/ZANDHIFORCE/Minuet_project/blob/codex/minuet-runnable-backend/docs/VALIDATION.md)

### Urination Detector · 서버·앱·장치의 데이터 흐름

캡스톤 과제에서 Django 서버, Java Android 라벨링 앱, 장치 연동과 현장 시험을 직접 수행했습니다. 사진 업로드 → 미분류 조회 → 라벨 갱신을 연결하고, 별도 단계로 준비한 모델의 추론·음성 경고까지 시연했습니다.

현장의 통신·설치 환경에 대응한 경험이 있습니다. 배경·날씨 변화에서 안정적인 탐지나 예방 효과를 검증한 시스템은 아닙니다.

[이미지·라벨 API](https://github.com/ZANDHIFORCE/UrinationDetector/blob/main/djangogirls/blog/views.py) · [API 안내](https://github.com/ZANDHIFORCE/UrinationDetector/blob/main/docs/API.md)

### AI Trainer · 외부 API와 웹 응답 연결

개인 개발한 Flask 서비스에서 운동 사진의 URL과 예시 이미지를 AI API에 전달하고 결과를 화면에 보여줍니다. 연구 평가에서는 예시·프롬프트 조건을 비교했습니다.

연구 보고서의 별도 평가 이미지 40장 기준 평균 F1은 MediaPipe 약 0.73, 초기 GPT 약 0.50, 개선 GPT 약 0.83이었습니다. 해당 평가셋의 보고값이며, 가중치 학습이나 모든 촬영 조건에서의 성능을 뜻하지 않습니다. 연구 자료의 공동 저자는 저장소에 표기했습니다.

[Flask 요청 처리](https://github.com/ZANDHIFORCE/AITrainer/blob/main/AiTrainer_flaskServer/app.py) · [평가와 한계](https://github.com/ZANDHIFORCE/AITrainer#모델-비교와-연구-기록)

## 추가 구현

[AiStock Backend](https://github.com/ZANDHIFORCE/AI-stock-backend): 2인 팀에서 백엔드·아키텍처를 담당했습니다. 세션·JWT 인증, JDBC 조건 검색, 예측 결과 이력을 구현했습니다. DB·AI는 팀원이 담당했으며 프로젝트는 미완성입니다.

각 저장소에 구현 범위, 코드 근거, 실행 조건과 남은 과제를 기록합니다.
