# monorepo-template

yarn berry workspace를 활용한 모노레포 프로젝트 템플릿.

# 사용법

1. npm install -g yarn (yarn 설치)
2. vscode 사용 시 pnp 정상 작동을 위하여 `yarn dlx @yarnpkg/sdks vscode` 명령어를 실행시켜주어야 합니다.

# tsconfig 설정

참조할 프로젝트의 경로를 root tsconfig.base.json의 references에 설정한다.
참조될 개별 프로젝트의 tsconfig에는 composite 및 declartion을 설정합니다.

# 새로운 프로젝트

1. **packages** 폴더 아래 새로운 폴더를 생성합니다.
2. package.json을 생성합니다.
   - 프로젝트 이름 앞에는 @를 붙이도록 합니다.
   - dependencies를 설정한다.
   - 참조할 프로젝트가 있다면 dependencies에 추가한다.
3. tsconfig.json을 생성합니다.
   - root의 tsconfig.base.json을 extends 후 필요한 옵션을 개별적으로 설정해줍니다.
