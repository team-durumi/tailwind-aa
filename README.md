# tailwind-aa

## tailwind-aa / durumi-archive
- 두 프로젝트 모두 tailwind-aa testbed로 사용합니다.(두 프로젝트 모두 Team Netlify에 연결되어 있습니다. )
- 서버 내려가도 되요. 안심하세요. 

## 개발준비(클론 - 참조 테마 업데이트)

```bash
git clone https://github.com/team-durumi/tailwind-aa.git
git submodule update --init --recursive
hugo mod npm pack
npm install
hugo server -D
```
- postcss 관련 에러가 뜨면, 테마관련 Pakage가 다운로드 안 되서 생기는 문제일 수 있어요. 
- marketing component에 내용이 없이 나온다면 data/marketing.yml 이 작성되어 있는지 확인하세요.

## 테마를 활용해서 별도로 hugo를 시작할 때는 테마 README를 참고하세요.
- https://github.com/team-durumi/tailwind-aa-theme/blob/master/README.md 

## theme component 를 업데이트 해주세요. 
- tailwind-aa-theme 도 아직은 성장중이에요. 새로 만든 component가 있다면 테마에 반영해주면 다음 프로젝트에 도움이 됩니다.