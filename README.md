# Github Action


<br>

# definition

### Event
- 깃허브에서 발생할 수 있는 이벤트 자체
- `ex` 커밋 내역을 푸시, 브랜치 머지, 이슈 등록 등

### Workflows 
- 특정 이벤트가 발생했을 때, 수행할 일을 명시하는 부분
- 1 ~ n개의 Job 조합으로 이루어질 수 있다

### Jobs
- Workflow 내부에 수행될 독립된 작업. 기본적으로 병렬적으로 수행된다
- 작업을 위한 단계를 step으로 표현할 수 있다

### Actions
- Job 내부에 shell script를 사용할 수도 있지만, action을 활용할 수 있다
- 기존에 미리 정의되어 있는 명령어, 재사용할 수 있는 명령들이 공개되어 있다
- `ex` npm 처럼 기존에 이미 만들어져 있는 도구들을 가져다 쓴다

### Runners
- 병렬적으로 존재하는 Job들을 실행하는 주체
- VM, 컨테이너 역할

<br>

---

# How to use

- github repository 안에 `.github/workflows/` 경로를 생성하여 yaml 파일을 생성

```yaml
name: 워크플로우_이름
on: [발생_이벤트]
jobs:
  잡_이름_1:
    runs-on: 사용할_가상머신
    steps:
      - 액션_이름: 수행구문
      - run: 쉘_스크립트_명령어

```






