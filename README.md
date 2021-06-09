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

## netlify CMS
- https://www.netlifycms.org/docs/hugo/#creating-a-new-site 앞 부분은 스킵
- ```static/admin``` 폴더에 index.html과 config.yml 을 추가합니다. (git-gateway 를 수정하지 않는다.)
- Front 경로 접근할 때 Netlify Identity를 확인할 수 있는 스크립트도 반드시 추가한다. 


# Build Capacity 

## 2배 분량 (items*20 )
- ```content/items/dummy``` 폴더에 2G 분량으로 복제 (115 ms -> Built in 20310 ms)
- Pages            |  411  
- Paginator pages  |   37  
- Non-page files   | 1271 

## 4배 분량 (items*40 )
- ```content/items/dummy``` 폴더에 2G 분량으로 복제 (115 ms -> Built in 75280 ms)
- Pages            |  779  
- Paginator pages  |   74  
- Non-page files   | 2511   