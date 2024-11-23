# 목차
1. [GIT Message convention](#GIT-Message-convention)
2. [Git Flow](#Git-Flow)

# GIT Message convention

## Commit message 구조

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

## Commit Types
- feat : 새로운 기능 추가
- fix : 버그 수정
- perf: 성능 개선
- docs : 문서 수정
- style : 코드 포맷팅, 세미콜론 누락, 코드 변경이 없는 경우
- refactor : 코드 리펙토링
- test : 테스트 코드, 리펙토링 테스트 코드 추가
- ci: ci 관련 파일 설정
- chore : 빌드 업무 수정, 패키지 매니저 수정

## 예시
```
feat: 사용자 정보 수정 기능 구현

- 기존 사용자 정보와 동일한지 체크하는 로직 구현
- User PUT API 추가

Refs: #123
Resolved #12, #34 
```

## 참고문서
[Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)

# Git Flow

![image](https://github.com/user-attachments/assets/504f1327-67c3-4b8d-860c-e9a36938741e)

## 메인 브랜치 (main)
- 역할: 제품 릴리스가 완료된 안정적인 코드를 저장하는 브랜치입니다.
- 명칭: main 또는 일부 프로젝트에서는 master를 사용합니다.
- 특징: 이 브랜치는 항상 배포 가능한 상태여야 하며, 버전 태그를 사용해 릴리스 이력을 기록합니다.
  
## 개발 브랜치 (develop)
- 역할: 새로운 기능 개발과 통합을 위한 기본 브랜치입니다.
- 명칭: 항상 develop으로 명명합니다.
- 특징: 새로운 기능과 변경 사항이 통합되며, main 브랜치로 병합되기 전에 테스트와 검증이 이루어집니다.

## 기능 브랜치 (feature/)
- 역할: 새로운 기능을 개발할 때 사용하는 브랜치입니다.
- 명칭: feature/기능명 or feature/이슈번호-기능명 (예: feature/login-page, feature/2-login-page)
- 생성 위치: develop 브랜치에서 생성합니다.
- 병합 위치: 작업 완료 후 다시 develop에 병합합니다.
- 특징: 각 기능은 독립적인 브랜치에서 개발되므로 코드 충돌 위험이 줄어듭니다.

## 릴리스 브랜치 (release/)
- 역할: 릴리스 준비를 위한 최종 버그 수정 및 QA 작업을 수행합니다.
- 명칭: release/버전명 (예: release/1.0.0)
- 생성 위치: develop 브랜치에서 생성합니다.
- 병합 위치: 작업 완료 후 main과 develop에 병합합니다.
- 특징: 릴리스 과정에서 작은 수정 사항을 적용하고, 최종 태그를 달아 릴리스를 기록합니다.

## 핫픽스 브랜치 (hotfix/)
- 역할: 배포된 제품에서 발견된 긴급 문제를 수정합니다.
- 명칭: hotfix/버전명 (예: hotfix/1.0.1)
- 생성 위치: main 브랜치에서 생성합니다.
- 병합 위치: 작업 완료 후 main과 develop에 병합합니다.
- 특징: 빠른 문제 해결이 목적이며, 변경 사항은 다음 릴리스에 포함됩니다.

## 참고문서
[A successful Git branching model](https://nvie.com/posts/a-successful-git-branching-model/), 
[Gitflow workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
