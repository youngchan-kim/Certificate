
# 📘 정보처리기사 Day 8 – 데이터베이스 관리 구조 개념 정리

---

## ✅ 1. 트랜잭션 (Transaction)

### 트랜잭션: 데이터베이스의 논리적 작업 단위

### ACID 특성

| 약어 | 의미 | 설명 |
|------|------|------|
| A | Atomicity (원자성) | 모두 성공하거나 전부 실패 (ROLLBACK) |
| C | Consistency (일관성) | 트랜잭션 전후 상태 일관성 유지 |
| I | Isolation (독립성) | 서로 간섭하지 않고 독립적으로 수행 |
| D | Durability (지속성) | COMMIT 이후 결과는 반드시 반영됨 |

### 제어 명령어

| 명령 | 설명 |
|------|------|
| COMMIT | 작업 확정 저장 |
| ROLLBACK | 변경사항 취소 |
| SAVEPOINT | 중간 지점 설정 (부분 ROLLBACK 가능) |

---

## ✅ 2. 병행 제어 (Concurrency Control)

### 병행 수행 시 문제점

| 문제 | 설명 |
|------|------|
| Lost Update | 두 트랜잭션이 동일 데이터 수정 → 덮어씀 |
| Dirty Read | 다른 트랜잭션의 미확정 데이터를 읽음 |
| Non-repeatable Read | 읽은 값이 중간에 수정됨 |
| Phantom Read | SELECT 시 보지 못한 행이 이후 생김 |

### 해결 방법
- Locking (공유/배타 락)
- 직렬화 (Serializability)

---

## ✅ 3. 무결성 제약조건 (Integrity)

| 제약조건 | 설명 |
|----------|------|
| PRIMARY KEY | 중복 ❌, NULL ❌ |
| FOREIGN KEY | 참조 관계 유지 |
| UNIQUE | 중복 ❌, NULL 허용 |
| NOT NULL | NULL 금지 |
| CHECK | 조건 만족해야 입력 가능 |
| DEFAULT | 기본값 자동 설정 |

---

## ✅ 4. 회복 (Recovery)

### 장애 복구 기법

| 기법 | 설명 |
|------|------|
| REDO | COMMIT된 트랜잭션 재수행 |
| UNDO | 취소된 트랜잭션 이전 상태로 복원 |
| CHECKPOINT | 복구 기준 시점 설정 |

---

✅ 위 개념을 바탕으로 트랜잭션, 병행 제어, 회복 전략 문제를 학습할 수 있습니다.
