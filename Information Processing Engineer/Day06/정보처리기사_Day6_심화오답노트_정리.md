
# 📘 정보처리기사 Day 6 – SQL 조건 함수 & 정렬 심화 오답노트 정리

## ✅ 채점 결과: 10 / 10

| 문항 | 너의 답 | 정답 | 정오 |
|------|---------|------|------|
| Q1   | 2       | 2    | ✅ |
| Q2   | 1       | 1    | ✅ |
| Q3   | 1       | 1    | ✅ |
| Q4   | 2       | 2    | ✅ |
| Q5   | 3       | 3    | ✅ |
| Q6   | 2       | 2    | ✅ |
| Q7   | 3       | 3    | ✅ |
| Q8   | 2       | 2    | ✅ |
| Q9   | 3       | 3    | ✅ |
| Q10  | 1       | 1    | ✅ |

---

## 🧠 복습 요약

### 🔹 NULL 처리 함수
- `NVL(A, B)` → A가 NULL이면 B
- `NVL2(A, B, C)` → A가 NULL이면 C, 아니면 B
- `COALESCE(A, B, ...)` → 첫 번째 NULL이 아닌 값 반환

### 🔹 CASE 조건 분기
```sql
CASE 
  WHEN 조건1 THEN 결과1
  WHEN 조건2 THEN 결과2
  ELSE 결과3
END
```
- 점수/급여/상태 분류 등에서 매우 자주 사용됨

### 🔹 DECODE
```sql
DECODE(성별, 'M', '남', 'F', '여', '기타')
```

### 🔹 GROUP BY + HAVING
```sql
SELECT 부서ID
FROM 사원
GROUP BY 부서ID
HAVING COUNT(*) >= 5;
```
- `GROUP BY` 필수 → `HAVING`만 단독 사용 시 오류 발생

### 🔹 ORDER BY 활용
- `ORDER BY 1 DESC` → 첫 번째 컬럼 기준 내림차순
- `ORDER BY 부서 ASC, 급여 DESC` → 복합 정렬 가능

---

✅ 실전 SQL 작성 연습과 함께 쓰면 완벽하게 체득 가능하다!  
Day 7부터는 조인 최적화, 뷰(VIEW), 인덱스, 시퀀스 등 실기용 구조로 넘어간다!
