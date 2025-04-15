
# 📘 정보처리기사 필기 Day 3 – 심화 오답노트 & 복습 정리

## ✅ 주제: SQL DDL – 심화 제약조건, ALTER, CREATE

---

## 🔁 오답노트 요약

### ❌ Q3. ALTER TABLE 문으로 할 수 없는 작업은?

- 너의 답: 4번 (제약조건 추가)
- 정답: 3번 (테이블 삭제)
- 해설:
  - `ALTER TABLE`: 구조 변경용 (컬럼 추가/삭제, 제약조건 추가/삭제)
  - ❌ 테이블 삭제는 `DROP TABLE 테이블명` 사용

---

## 📊 채점 요약

| 문항 | 너의 답 | 정답 | 정오 |
|------|---------|------|------|
| Q1   | 2       | 2    | ✅ |
| Q2   | 3       | 3    | ✅ |
| Q3   | 4       | 3    | ❌ |
| Q4   | 3       | 3    | ✅ |
| Q5   | 3       | 3    | ✅ |

---

## 📌 복습 핵심 요약

### 🔹 CHECK 제약조건
- 입력된 값이 **지정 조건**을 만족하는지 확인
- 예: `CHECK (Age >= 18)`

### 🔹 DEFAULT 제약조건
- 값을 입력하지 않았을 때 **기본값 자동 입력**
- 예: `InStock INT DEFAULT 100`

### 🔹 ALTER TABLE
| 명령 | 설명 |
|------|------|
| `ALTER TABLE ADD` | 컬럼 추가 |
| `ALTER TABLE DROP COLUMN` | 컬럼 삭제 |
| `ALTER TABLE ADD CONSTRAINT` | 제약조건 추가 |
| `ALTER TABLE DROP CONSTRAINT` | 제약조건 삭제 |
| `DROP TABLE` | 테이블 삭제 (ALTER로는 ❌ 불가) |

### 🔹 복합키
- `PRIMARY KEY (A, B)` → **A + B 조합**이 유일해야 함
- A 또는 B 개별로는 중복 가능

### 🔹 컬럼 수준 제약조건
- `NOT NULL`, `DEFAULT` 등은 **컬럼 정의 시 직접 지정 가능**
- `FOREIGN KEY`는 보통 테이블 수준에서 설정

---

✅ 실무에서도 자주 사용하는 명령들이므로 실제 SQL 문법까지 같이 익히는 걸 추천!
