# Chapter 02 제출 답안. VS Code에서 시작하는 데이터 분석 환경

> 최종 파일은 개인 GitHub 저장소의 `chapter02/chapter02.md`로 저장하는 것을 권장합니다.

## 0. 제출 정보

- 이름: 권영서
- GitHub ID: kys02101-cmd
- 개인 저장소: `llm-data-analysis-study`
- 작성일: 2026-09-16
- 운영체제: 윈도우

### 최종 제출 URL

```text
https://github.com/kys02101-cmd/llm-data-analysis-study/blob/main/chapter02/chapter02.md
```

---

## 1. Python과 Git 환경 확인

### 실행 내용

```text
python --version 또는 py --version
git --version
```

### 실행 결과

```text
PS C:\WINDOWS\system32> python --version
Python 3.14.7
PS C:\WINDOWS\system32> git --version
git version 2.55.0.windows.5
```

### Evidence

![Python과 Git 버전](images/step01_versions.png)

### 결과 관찰

처음에는 설치가 되어있지 않아 오류 메시지가 떴지만, 설치 이후 Python 버전 3.14.7과 git 버전 2.55.0.windows.5 버전이 정상적으로 출력됐습니다.

### 나의 해석과 판단

정상적으로 작동하므로 현재 환경이 수업 실습에 적합합니다.

### 업무·분석적 의미

설치가 되어있는지 작동이 되는지 먼저 확인해야 이후 작업이 가능하며, 버전에 따라 가능한 분석 방법이 다를 수 있기 때문에 확인할 필요가 있습니다.

### 한계와 추가 확인 사항

최신 버전인지 추가로 확인해 볼 수 있습니다.

---

## 2. 저장소와 `.venv` 준비

### 수행 내용

- [x] 공식 Public 저장소 clone
- [x] 프로젝트 루트 확인
- [x] `.venv` 생성
- [x] `.venv` 활성화
- [x] `requirements.txt` 설치

### 핵심 실행 결과

```text
현재 프로젝트 경로: C:\Users\Administrator\Documents\개발\llm-data-analysis-course
터미널 Python 실행 파일: C:\Users\Administrator\Documents\개발\llm-data-analysis-course\.venv\Scripts\python.exe
가상환경 활성화 여부: 활성화됨
패키지 설치 결과: 설치됨
```

### Evidence

![가상환경과 Python 경로](images/step02_venv.png)

### 결과 관찰

C:\Users\Administrator\Documents\개발\llm-data-analysis-course\.venv\Scripts\python.exe

### 나의 해석과 판단

시스템 Python과 프로젝트별 .venv를 분리하면 프로젝트마다 필요한 패키지와 버전을 독립적으로 관리할 수 있으므로, 한 프로젝트에서 뭔가를 변경해도 다른 프로젝트에 영향을 주지 않게끔 할 수 있어 유용합니다.

### 업무·분석적 의미

가상환경을 사용하면 프로젝트에 필요한 Python 패키지와 버전을 동일하게 관리할 수 있어, 다른 사람이 같은 프로젝트를 실행할 때도 동일한 환경을 쉽게 재현할 수 있습니다.

### 한계와 추가 확인 사항

회사 PC에서 PowerShell에서 가상환경 활성화 스크립트 실행이 제한되는 문제가 있었습니다.

---

## 3. VS Code 인터프리터와 Jupyter 커널 연결

### 확인 결과

```text
VS Code Python 인터프리터:
Notebook sys.executable:
Notebook Path.cwd():
```

### Evidence

![VS Code 인터프리터와 Notebook 커널](images/step03_kernel.png)

### 결과 관찰

터미널 Python과 Notebook Python이 같은 `.venv`인지 작성하세요.

### 나의 해석과 판단

둘이 다를 경우 어떤 문제가 발생할 수 있는지 작성하세요.

### 업무·분석적 의미

`ModuleNotFoundError` 같은 환경 오류를 줄이는 데 어떤 도움이 되는지 작성하세요.

### 한계와 추가 확인 사항

커널 이름만 보고 판단하면 안 되는 이유 등 추가 확인 사항을 작성하세요.

---

## 4. 샘플 데이터와 Notebook 실행 검증

### 확인 결과

```text
DATA_DIR 존재 여부:
customers.csv 존재 여부:
customers.shape:
주요 컬럼:
```

### Evidence

![customers 데이터 정상 로드](images/step04_customers.png)

### 결과 관찰

`customers.head()`, shape, 컬럼 결과에서 직접 확인한 사실을 작성하세요.

### 나의 해석과 판단

이 단계까지 성공했다면 어떤 구성 요소가 정상 연결되었다고 판단할 수 있는지 작성하세요.

### 업무·분석적 의미

분석 전에 최소 스모크 테스트를 하는 이유를 작성하세요.

### 한계와 추가 확인 사항

현재는 환경 연결만 확인했으며 데이터 품질은 아직 검증하지 않았다는 점을 작성하세요.

---

## 5. 오류 해결 기록

실습 중 오류가 있었다면 작성합니다. 오류가 없었다면 `해당 없음`이라고 적습니다.

### 오류 메시지

```text
민감정보를 제거한 실제 오류
```

### 원인 후보

1.
2.
3.

### 내가 확인한 순서

1.
2.
3.

### 해결 방법

```text
실제로 적용한 해결 방법
```

### Evidence

![오류 해결 결과](images/step05_troubleshooting.png)

### 나의 해석과 판단

왜 해당 원인이 가장 가능성이 높다고 판단했는지 작성하세요.

### 한계와 추가 확인 사항

보안 정책 변경, 무분별한 삭제처럼 시도하지 않은 조치와 이유를 작성하세요.

---

## 6. Secret 보호 확인

- [ ] `.env`는 Git 추적 대상이 아닙니다.
- [ ] 실제 API Key를 코드에 작성하지 않았습니다.
- [ ] 캡처 화면에 Token/비밀번호가 없습니다.
- [ ] `.venv`를 Git에 올리지 않습니다.

### Evidence

필요한 경우 `git status`, `.gitignore` 확인 화면을 첨부합니다.

![Secret 보호 확인](images/step06_security.png)

### 나의 해석과 판단

환경 파일과 비밀정보를 분리해야 하는 이유를 작성하세요.

---

## 7. Chapter 02 최종 회고

### 가장 중요했다고 생각한 환경 설정 1가지

```text
작성하세요.
```

### 그 이유

```text
작성하세요.
```

### 다음 Chapter에서 재사용할 환경 체크 3가지

1.
2.
3.

### 현재 환경의 한계 또는 주의점

```text
작성하세요.
```

---

## 최종 제출 체크

- [ ] 핵심 Evidence 4~7장을 첨부했습니다.
- [ ] 단순 캡처가 아니라 관찰과 판단을 작성했습니다.
- [ ] Secret/개인정보가 없습니다.
- [ ] GitHub에서 이미지가 정상 표시됩니다.
- [ ] 개인 저장소에 `chapter02/chapter02.md`를 업로드했습니다.
- [ ] 저장소 URL이 아니라 최종 파일 URL을 제출합니다.
