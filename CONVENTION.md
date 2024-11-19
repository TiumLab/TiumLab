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
