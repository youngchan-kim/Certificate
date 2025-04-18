# 정보처리기사 Day6 복습 오답노트 정리

## 📌 데이터베이스 - 서브쿼리

### 🔹 서브쿼리 사용 불가능한 경우
- SELECT 절의 `GROUP BY`, `ORDER BY` 내부에는 서브쿼리 사용 불가
- `UNION`, `INTERSECT` 등과 결합된 서브쿼리는 SELECT 절에서 직접 사용 제한 있음
- `FROM` 절 안의 서브쿼리는 반드시 별칭(alias) 필요

### 🔹 서브쿼리 형태별 요약
- 단일행 서브쿼리: `=`, `>`, `<`, `<=`, `>=`, `<>`
- 다중행 서브쿼리: `IN`, `ANY`, `ALL`
- 상관 서브쿼리: 외부 쿼리 컬럼 참조 필요

---

## 📌 정규화 관련

### 🔹 정규형
- 제1정규형(1NF): 원자값
- 제2정규형(2NF): 부분 함수 종속 제거
- 제3정규형(3NF): 이행적 함수 종속 제거
- BCNF: 결정자이면서 후보키가 아닌 것 제거

### 🔹 오답 포인트
- 정규형 간 구분 헷갈림
- 특히 2NF, 3NF를 구분 못함 → **부분 함수 종속 vs 이행적 함수 종속** 구분 연습 필요

---

## 📌 트랜잭션과 병행제어

### 🔹 트랜잭션 특성 (ACID)
- Atomicity (원자성)
- Consistency (일관성)
- Isolation (고립성)
- Durability (지속성)

### 🔹 병행제어 기법
- 로킹 기반: 공유락/배타락
- 낙관적 기법: 충돌 가능성 낮을 때
- 타임스탬프 기법

---

## 🧠 복습 포인트 요약
- 서브쿼리 문법 위치: `SELECT`, `FROM`, `WHERE` 사용 위치 및 제약조건 암기
- 정규화 순서 및 개념 암기
- 트랜잭션 ACID 확실히 정리
- 병행제어 기법들 사례로 구분 연습 필요