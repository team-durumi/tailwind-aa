# aa.durumi.io

## tailwind-aa / durumi-archive
- 두 프로젝트 모두 tailwind-aa testbed로 사용합니다.(두 프로젝트 모두 Team Netlify에 연결되어 있습니다. )
- 서버 내려가도 되요. 안심하세요. 
- markeiting base 여서 블로그를 여기에 작성합니다.

## Git Submodule을 제거합니다.
- 설치되어 있던 다수의 submoudule을 제거합니다.
- git 내에 있던 모듈을 삭제합니다. 
- 빈 폴더를 삭제합니다.  

```bash
git submodule deinit -f themes/tailwind-aa-theme
rm -rf .git/modules/themes/tailwind-aa-theme
git rm -f tailwind-aa-theme 
```

```bash
git clone https://github.com/team-durumi/tailwind-aa.git
hugo mod npm pack
npm install
hugo server -F --cleanDestinationDir
```
- postcss 관련 에러가 뜨면, 테마관련 Pakage가 다운로드 안 되서 생기는 문제일 수 있어요. 
- marketing component에 내용이 없이 나온다면 data/marketing.yml 이 작성되어 있는지 확인하세요.

### go module init & update
- https://gohugo.io/hugo-modules/use-modules/#update-modules
```
go mod init github/team-durumi/tailwind-aa-theme
go get -u github.com/team-durumi/hugo-search-fuse-js-aa
```
- 휴고 server 하는 시점에 자동으로 go get으로 버전에 맞는 테마를 갖고오면서 go.mod 파일이 변경되고, go.sum 파일도 가져옴. 

## 검색
- go module로 설치한 search-fuse-js-aa 에 search.js 를 불러오지 못 하는 문제가 있어서 경로 변경
```
Error: Error building site: failed to render pages: render of "page" failed: "/Users/woonjjang/hugo/tailwind-aa/layouts/_default/search.html:85:24": execute of template failed: template: _default/search.html:85:24: executing "footer" at <readFile "themes/hugo-search-fuse-js-aa/static/js/search.js">: error calling readFile: stat /Users/woonjjang/hugo/tailwind-aa/themes/hugo-search-fuse-js-aa/static/js/search.js: no such file or directory
```

## netlify CMS
- https://www.netlifycms.org/docs/hugo/#creating-a-new-site 앞 부분은 스킵
- ```static/admin``` 폴더에 index.html과 config.yml 을 추가합니다. (git-gateway 를 수정하지 않는다.)
- Front 경로 접근할 때 Netlify Identity를 확인할 수 있는 스크립트도 반드시 추가한다. 
- items는 depth가 있어서 md file을 모두 인식하지 못 함. (post로 변경)

## multilingual
- content 폴더로 구분하는 방법이 있을텐데, 복잡해질 가능성이 높아서 content.langcode 폴더로 동일하게 만들어서 복사하는 방법

# Data

- 공유드라이브/aa/tailwind-aa/items
- https://drive.google.com/drive/u/1/folders/1TGlIbLoGAh6XlymvZk59Wcj7CjMz1QZK


# next aa-0.2

- (예정)design system UI 0.2 - 다이나믹 전시, 리서치가이드, 콘텐츠
- (예정)다국어 관련 데이터 처리 및 UI 기준 개발 
- (예정)전시 / 리서치가이드 편집 
- (예정)Ubuntu 서버 기반의 자동화 
- (예정)폐쇄적 아카이브 운영 개발

