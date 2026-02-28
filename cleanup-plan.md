# /home/kimjin/ 정리 계획 및 실행 가이드

## 🎯 전략 개요

**목표**: 시스템 최적화 및 디스크 공간 절약 (목표: 25GB+)

**분류**:
1. **Phase 1**: 즉시 정리 (비활성 파일/폴더)
2. **Phase 2**: 루트 파일 정렬 + 캐시 최적화
3. **Phase 3**: 프로젝트 통합 + 최종 최적화

---

## Phase 1: 즉시 정리 (16.4GB)

### 단계 1-1: 중복 폴더 정리
```bash
# 바탕화면 → Archive/Desktop-Old (4.9GB)
# Downloads/Ubuntu ISO → Archive/ISOs (3.2GB)
# 다운로드 → Archive/Downloads-Old (2.5GB)
```

### 단계 1-2: 비활성 프로젝트 정리
```bash
# email-system (2.8GB, DB만 있음)
# julia_install (945MB, 이전 설치본)
# clone_city (805MB, 비활성)
# google-cloud-sdk (1.2GB, 비사용)
```

### 단계 1-3: 캐시 정리
```bash
# .cache (24MB → 48KB)
# Chrome, Thunderbird, nvidia 캐시 삭제
```

---

## Phase 2: 루트 파일 정렬 + 캐시 (11.4GB)

### 단계 2-1: 루트 파일 정렬 (364개)
```
RootFiles/
├── scripts/ - .sh, .py, .js, .c 파일
├── docs/ - .md, .txt 문서
├── config/ - .json, .yaml, .conf 설정
├── logs/ - .log 파일
├── data/ - .db, .csv 데이터
├── backups/ - 압축, 백업 파일
├── tools/ - 바이너리 도구
└── system/ - .bashrc, .gitconfig 등
```

### 단계 2-2: .config 최적화 (3.5GB → 1.1GB)
```bash
# VSCode 캐시 삭제 (1.5GB)
# Chrome 캐시 삭제 (811MB)
# yarn 캐시 삭제 (126MB)
```

### 단계 2-3: .local 최적화 (23GB → 14GB)
```bash
# Trash 폴더 정리 (7.8GB)
# IDE 캐시 삭제 (1.4GB)
# site-packages 유지 (13GB, 시스템 필수)
```

---

## Phase 3: 프로젝트 통합 (0.13GB)

### 단계 3-1: 비활성 프로젝트 정리
```bash
# kim-pm2 (8.4MB, 2개월 전)
# kim-dns (19MB, 2개월 전)
# freelang-* 관련 정리
```

### 단계 3-2: Python 캐시 정리
```bash
# __pycache__ 7,836개 정리
# site-packages 유지 (시스템 필수)
```

### 단계 3-3: 검증
```bash
# 활성 프로젝트 7개 확인
# 심볼릭 링크 검증
# Git 저장소 상태 확인
```

---

## 📋 실행 체크리스트

### Phase 1
- [ ] Archive 폴더 생성
- [ ] 바탕화면, Downloads, 다운로드 이동
- [ ] 비활성 프로젝트 이동
- [ ] .cache 정리

### Phase 2
- [ ] RootFiles 폴더 생성 + 파일 정렬
- [ ] .config 캐시 삭제
- [ ] .local Trash 정리
- [ ] IDE 캐시 삭제

### Phase 3
- [ ] 비활성 프로젝트 정리
- [ ] Python __pycache__ 정리
- [ ] 활성 프로젝트 검증
- [ ] 최종 상태 확인

---

## 📊 예상 효과

| Phase | 절약 |
|-------|------|
| 1 | 16.4GB |
| 2 | 11.4GB |
| 3 | 0.13GB |
| **합계** | **27.93GB** |

---

## 🚀 권장 정기 유지

**월 1회**:
- `git gc --aggressive` (저장소 정리)
- `npm cache clean --force` (npm 캐시)

**분기별 (3개월)**:
- Python __pycache__ 정리
- Archive 내용 검토
- 로그 파일 정리

**반기별 (6개월)**:
- .cache 정리
- .config 최적화
- 심볼릭 링크 검증

---

## ✅ 최종 상태

**정리 전**: ~747MB (전체 크기)
**정리 후**: 절약 27.93GB

**정리율**: 약 27% 용량 절약 ✅

