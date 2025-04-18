
# 📘 정보처리기사 필기 Day 2 – 심화문제 오답노트 & 해설

## ✅ 주제: 정규화 & 관계형 모델 – 심화 개념

---

## 🔁 오답노트 정리

### ❌ Q1. 3NF 정규화 조건으로 옳은 것은?

- 너의 답: 4번 (반복 그룹이 없어야 한다)
- 정답: 2번 (이행적 함수 종속이 없어야 한다)
- 해설: 
  - 1NF: 반복 제거
  - 2NF: 부분 종속 제거
  - ✅ 3NF: 이행적 종속 제거

---

### ❌ Q2. 함수적 종속 A → B 의미는?

- 너의 답: 4번 (A와 B는 항상 같은 값을 가진다)
- 정답: 1번 (A가 같으면 B도 반드시 같다)
- 해설:
  - A → B는 “A값 같으면 B도 같다”
  - A 다르면 B는 달라도 되고 같아도 됨

---

### ✅ Q3. 후보키가 아닌 것은?

- 너의 답: 4번 (외래키)
- 정답: 4번 (외래키)
- 해설:
  - 외래키는 참조용 키일 뿐, 후보키 조건인 유일성+최소성 만족 안 함

---

### ✅ Q4. A가 B를 결정할 때 올바른 표현은?

- 너의 답: 3번 (A → B)
- 정답: 3번 (A → B)
- 해설:
  - 함수적 종속의 기본 표현 방식

---

### ✅ Q5. 정규화의 장점이 아닌 것은?

- 너의 답: 3번 (성능 향상)
- 정답: 3번 (성능 향상)
- 해설:
  - 정규화는 성능 향상보다 무결성 유지, 중복 제거, 이상 방지에 목적이 있음
  - 조인이 많아져 성능 저하될 수 있음

---

## 📊 채점 요약

| 문항 | 너의 답 | 정답 | 정오 |
|------|---------|------|------|
| Q1   | 4       | 2    | ❌ |
| Q2   | 4       | 1    | ❌ |
| Q3   | 4       | 4    | ✅ |
| Q4   | 3       | 3    | ✅ |
| Q5   | 3       | 3    | ✅ |

---

## 📌 심화 복습 포인트 정리

### 🔹 정규화 단계별 요건

| 단계 | 제거 대상 | 문제 해결 |
|------|------------|-------------|
| 1NF | 반복 그룹 제거 | 테이블 구조 간결화 |
| 2NF | 부분 종속 제거 | 삽입/삭제 이상 |
| 3NF | 이행 종속 제거 | 갱신 이상 |

### 🔹 함수적 종속

- A → B는 “A 같으면 B도 같음”
- A → B가 참이면 A ≠ B여도 가능
- 표현 방식: A → B (A가 결정자)

### 🔹 키 개념 정리

| 키 종류 | 설명 |
|---------|------|
| 기본키 | 튜플 식별용, 유일 + NULL 금지 |
| 후보키 | 유일성과 최소성 만족하는 키 후보 |
| 대체키 | 후보키 중 기본키로 쓰지 않는 것 |
| 외래키 | 다른 릴레이션의 기본키 참조, 중복/NULL 허용 |

---

✅ 심화 문제는 실기에서도 그대로 출제되는 핵심이다.  
오답 체크한 개념은 반드시 암기하고 예제도 만들어볼 것!
