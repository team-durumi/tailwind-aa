# 범용적으로 사용할 수 있는 aa-starter-theme

## 진행

- featured item 기존 블로그 폼으로 진행한다. / video-item 페이지를 노출해 본다. 
- 목록을 위한 aside  부분
- UI 기준에 잡혀있는데로, 테마 설정을 시도한다. (color, typo)
- alpinejs 를 사용하도록 할 수 도 있고, js 적용을 다시 결정할 수도 있다.
- recent-items 같은 section은 고정되지 않은 데이터와 연결하는 부분 (app쪽 데이터에 맞는듯) / 전체 목록과 최신 part
- 다른 faq를 만들어보면서 alphinejs를 적용해 봅시다. (헤더, 슬라이드, faq )


## data/marketing info
- 외부에 일반 사람들에게 편집을 전달해도 이상하지 않을 dummy text
- user information(전역 설정)도 marketing.yml에 표시한다. 
- section UI 를 만들어서 개발 -> marketing.yml에 데이터 교체(해당 파일만 교체해도 partial 파일들은 크게 손 대지 않아도 된다.)


## content item metadata
- 1타입 정도가 marketing.yml에 있어도 더미로 만들 때 뷰가 깨지지 않을 수 있겠군. 


## 해결
- html에 찍고 있는 partial에 데이터를 data/marketing.yml 로 옮겨본다.(파일작성시_만 허용됨)


## As a Project

```bash
npm install
hugo server
```

## As a Theme

Import `github.com/bep/hugo-starter-tailwind-basic/v2` (use `github.com/bep/hugo-starter-tailwind-basic` if you want/need Tailwind 1.x.) into your project, and then run:

```bash
hugo mod npm pack
npm install
```

You need to add this to your `config.toml` (the stats are used by the CSS purging):

```toml
[build]
writeStats = true
```

Then run your project as usual.
