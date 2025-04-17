
# 📘 정보처리기사 Day 7 – SQL 구조 심화 오답노트 & 해설 정리

## ✅ 채점 결과: 7 / 10

| 문항 | 너의 답 | 정답 | 정오 |
|------|---------|------|------|
| Q1   | ?       | 2    | ❌ |
| Q2   | ?       | 2    | ❌ |
| Q3   | 1       | 1    | ✅ |
| Q4   | 3       | 3    | ✅ |
| Q5   | 1       | 4    | ❌ |
| Q6   | 2       | 2    | ✅ |
| Q7   | ?       | 2    | ❌ |
| Q8   | 3       | 3    | ✅ |
| Q9   | 3       | 1    | ❌ |
| Q10  | 3       | 3    | ✅ |

---

## ❌ 틀린/모르겠는 문제 상세 해설

### Q1. VIEW에서 DML 제한되는 경우
- 정답: 2번 (**GROUP BY나 집계 함수가 포함된 VIEW**)
- 이유: 집계 함수나 그룹핑이 포함된 VIEW는 데이터의 정확한 **행 식별이 어려워** DML이 제한됨  
- 예: `SELECT 부서ID, COUNT(*) FROM 사원 GROUP BY 부서ID` → UPDATE/INSERT 불가

---

### Q2. INDEX 성능 향상 어려운 경우
- 정답: 2번 (**WHERE 절이 없는 전체 조회 쿼리**)
- 이유: INDEX는 **조건 필터링이 있을 때**만 활용됨  
→ `SELECT * FROM 테이블`은 **풀스캔** 발생 → INDEX 사용 불가

---

### Q5. CURRVAL 사용 조건
- 정답: 4번 (오류 발생)
- 이유: `CURRVAL`은 반드시 `NEXTVAL`을 먼저 호출해야 값을 참조할 수 있음  
→ 세션 내 `NEXTVAL` 호출이 없으면 `ORA-08002: sequence CURRVAL is not yet defined` 오류 발생

---

### Q7. 잘못된 VIEW SQL
- 정답: 2번  
```sql
CREATE VIEW V2 AS SELECT 이름, COUNT(*) FROM 사원 GROUP BY 이름;
```
- 문제점: COUNT 사용된 SELECT에 **집계 외 컬럼이 존재** → GROUP BY 대상이 충분하지 않으면 오류 발생하거나 **DML 제한 VIEW**가 생성됨

---

### Q9. INDEX 자동 생성
- 정답: 1번 (**PRIMARY KEY 제약조건 설정 시 자동 생성**)
- 설명: `CREATE TABLE` 시 `PRIMARY KEY`를 설정하면 내부적으로 INDEX가 자동 생성됨

---

## ✅ 맞춘 문제 요약 정리

### Q3. 함수 기반 INDEX 사용 가능
- 예: `CREATE INDEX ON LOWER(이메일)` → `WHERE LOWER(이메일)` 조건과 일치 → INDEX 사용 가능  
→ 정답: 1번 (INDEX 사용되지 않음 상황 **아님**)

---

### Q4. OUTER JOIN 사용 목적
- 정답: 3번  
- 사용 목적: 일치하지 않는 값도 **NULL 포함하여 출력**할 수 있게 함

---

### Q6. INDEX 성능 저하 상황
- 정답: 2번 (자주 UPDATE/DELETE 되는 경우)  
- 이유: INDEX는 항상 유지되므로, 자주 변경되면 **쓰기 성능 저하** 발생 가능

---

### Q8. 시퀀스 사용 목적
- 정답: 3번 (자동 증가 고유값 부여)  
- 예: 주문번호, 회원번호 등

---

### Q10. `LIKE '%123'` → 문자열 끝 패턴 검색
- 정답: 3번 (검색 속도 느림)  
- 이유: `%`로 시작되면 INDEX 사용 거의 불가능 → **풀스캔 유발**

---

## 🔁 요약

| 항목 | 요점 정리 |
|------|-----------|
| VIEW | 집계 포함 시 DML 제한 있음 |
| INDEX | 조건 없는 전체 조회는 INDEX 무의미 |
| CURRVAL | NEXTVAL 호출 전 사용 시 오류 |
| 자동 INDEX | PRIMARY KEY 설정 시 자동 생성 |
| OUTER JOIN | 누락 데이터 포함 출력 가능 |

---

✅ 다음 문제에서는 VIEW로 DML 가능한 구조, INDEX 사용 전략, SEQUENCE 예외 처리를 직접 구성해보는 실전 문제로 넘어갈게!
