```mermaid
flowchart TD
    A[사용자 요청 입력<br>(Prompt, 질문 등)] --> B[검색 요청 로그 수집<br>(RAG Retrieval)]
    B --> C[검색 결과 출력 로그 수집]
    C --> D[모델 입력 생성<br>(프롬프트 + 검색결과)]
    D --> E[모델 응답 출력<br>(AI 응답 메시지)]
    E --> F[최종 사용자 출력<br>(서비스 결과 메시지)]

    subgraph "로그 적재 지점"
        B
        C
        D
        E
        F
    end

    F --> G[로그 적재<br>(DB 또는 로그 수집기)]
    G --> H[로그 관리/조회 시스템<br>(조건 검색, 소요 시간 분석 등)]
```
